# 📄 **[https://dillinger.io/ALGORITHIA_REQ_CD_TI_ELK_QUITARANONIMATO_PERSONACANAL_v2.02.03.xlsx](ALGORITHIA_REQ_CD_TI_ELK_QUITARANONIMATO_PERSONACANAL_v2.02.03.xlsx)** 
___

## 01_Control_de_Versiones
| : 0 | Cristal Data Control de Versiones | : 2 | : 3 | : 4 |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
|  | Versionamiento |  |  |  |
|  | No. de Versión | Fecha de cambio | Autor | Descripción |
|  | 1 | 2023-02-17 00:00:00 | Juan Carlos Cifuentes | Generación de Versión 1 del Documento |
|  | 1.1 | 20/07/2023 | Juan Carlos Cifuentes | Modificación de la estructura de la tabla de anonimato en zona curada |
|  | 1.01.01 | 22/08/2023 | Juan Carlos Cifuentes | Modificación del proceso para contemplar el filtro de Colores desde la Tabla RAW |
|  | 1.01.02 | 2023-12-09 00:00:00 | Juan Carlos Cifuentes | Adición de los campos banderadocumentodigital, y banderamercadotecnia a la tabla desde la zona curada, para validar los requerimientos legales |
|  | 1.01.03 | 15/9/2023 | Juan Carlos Cifuentes | Modificación del Catálogo de Tipo de Venta por temas de gobernanza |
|  | 1.01.04 | 25/9/2023 | Juan Carlos Cifuentes | Modificación de la Familia y Dominio, asi como eliminar el filtro de País en la consulta del paso 4 |
|  | 2.01.01 | 2023-11-17 00:00:00 | Juan Carlos Cifuentes | Generación del Crystal cd\_ekt\_pressupuestos\_anonimato, donde se disponibiliza la información de Red Unica, Tienda Física EKT, MasterID, CeCos, SKUs Comercios y SKUs SIE.<br>Se adicionan los filtros de Punto de Venta y filtrar los presupuestos con longitud 19 |
|  | 2.01.02 | 2023-11-21 00:00:00 | Juan Carlos Cifuentes | Modificación del paso 8 para indicar los campos relacionados a los productos de los presupuestos necesarios y el DER de la pestaña 5 |
|  | 2.01.03 | 2023-11-22 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>•&emsp;Paso 1: Se cambia el comparador == por like ya que se debe quedar con los presupuestos que contenga las palabras COLOR, TEST o PRUEBA en el cliente<br>•&emsp;Paso 4: Se excluye la información de Elektra.com (fisucursal != 9797) de los presupuestos<br>•&emsp;Paso 5: Se excluye la información de Elektra.com (fisucursal != 9797) de los pedidos y cliente\_unico<br>•&emsp;Paso 7: Aclaración de expandir la estructura detalle\_presupuesto a fila<br>•&emsp;Se corrige el nombre de la variable descripcionTipoVenta en los pasos 5, 7,8,9,10 y 11<br> |
|  | 2.01.04 | 2023-01-10 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>•&emsp;Adición de la lógica de constucción<br> |
|  | 2.01.5 | 2023-01-10 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>•&emsp;Adición de la lógica de constucción<br> |
|  | 2.01.6 | 2023-01-23 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>•&emsp;Adición de campos sensibles para el cruce de la información,<br> |
|  | 2.01.7 | 2023-02-08 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>• Apertura del Paso 15, con lo que se modifica desde el paso 11 hasta el 16<br>•Corrección del paso 22, moviendo los criterios de rekación a los filtros<br>Adicion del paso 25 para contemplar el mes anterior al último presupuesto<br> |
|  | 2.01.8 | 2023-02-12 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>A nivel presupuesto contemplar dos estatus adicionales a CeCos y dos campos solicitados por el usuario<br>• Eliminación de paso 1 y 2 en persona-envio<br>•Mover el paso 25 al 3<br>•Contemplar la modificación de la estandarización express generando un paso 10 con indicadores consolidados<br>•Uso de la tabla paso 10 para cruzar con datos\_contacto\_master<br>•Modificación de las marcas para construirse con base al masterID<br> |
|  | 2.01.09 | 29/2/2023 | Juan Carlos Cifuentes | Modificación de:<br>Modificación del Paso 4,6,7,8,9 y 10 para incluir la calificación del correo y celular para el cruce eidentificación del MasterID<br>Modificación del paso 8 quitando eldescencriptar de la tabla B (Frecuencia)<br>Adición de criterio en curado dado la última regla del correo para la estandarización<br> |
|  | 2.01.10 | 2023-02-14 00:00:00 | Juan Carlos Cifuentes | Modificación de los nombres para alinear a marco de nomenclatura del lake<br> |
|  | 2.02.01 | 2023-02-17 00:00:00 | Juan Carlos Cifuentes | Requerimiento de IT se documentaran por separado las entidades, contemplando en este documento la entidad persona<br> |
|  | 2.02.02 | 2024-07-29 00:00:00 | Oswaldo Chávez Mogollán | Actualización de cliente unico, masterid, e indicadores: EsPedido, EsPptoCredito, EsCredito, ClienteUnico<br> |
|  | 2.02.03 | 2024-09-02 00:00:00 | Oswaldo Chávez Mogollán | Actualización de espersonaconocida<br> |

## 02_CD_Presentación_Producto
| : 0 | Cristal Data Presentación del Producto | : 2 |
| --- | --- | --- |
|  |  |  |
|  | Información general del Cristal Data |  |
|  | Nombre(s) tabla(s) Final(es): | cd\_ekt\_prospecto\_cte\_canales\_envio |
|  | Descripción: | Cristal Data que permitirá sacar del anonimato a los clientes que envían información del presupuesto. Para esto se disponibiliza dos tablas para responder las preguntas:<br>- Presupuestos: ¿qué presupuestos se han enviando a los Clientes/Prospectos ?¿Que productos se presupuestan por tienda y región?¿qué presupuestos se convirtieron en un pedido?<br><br>Este Crystal dara respuesta a la presentación de DG y también se podrá identificar que presupuestan los clientes para entender y mejorar la experiencia del cliente, permitiendo tener datos para proponer campañas o comunicados entendiendo que presupuestan y si es a crédito o contado |
|  | Familia: | Cliente y presupuesto |
|  | Empresa: | Elektra |
|  | Dominio: | Personas |
|  | Periodicidad de la ejecución (diaria,semanal, mensual, et.): | Diaria |
|  | Tipo de Actualización (full, delta, etc. | Delta |
|  | Profundidad Histórica: | Requiere desde junio de 2023 en adlentare |
|  | Nivel de Granularidad | Presupuesto y SKU de tienda física EKT |
|  | Grupos de Usuarios | Karen Altagracia Olivo Santana y Alfa Berenice |

## 03_CD_Insumos
| : 0 | Cristal Data Insumos | : 2 | : 3 | : 4 | : 5 | : 6 | : 7 | : 8 | : 9 | : 10 | : 11 | : 12 | : 13 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Detalles de los Insumos de los cuales depende |  |  |  |  |  |  |  |  |  |  |  |  |
|  | No. | Plataforma | Objeto | Esquema | Tabla | Campo | PK (1=pk, 2=fk, 0= Otro) |  |  |  |  |  |  |
|  | 1 | Cloudera kio |  | cd\_ekt\_bdclientes | cd\_ekt\_prospecto\_cte\_presupuesto | TiendaID | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | PresupuestoID | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | SkuId | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | esPedido | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteUnico | 0 |  |  |  |  |  |  |
|  | 2 | Cloudera kio |  | cu\_bdekt | cu\_ekt\_clientes\_prospecto | PaisID | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | NombreDocumento | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | TicketID | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteCorreo | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | DocumentoID | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | NumeroEconomicoSucursal | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | tipocanalid | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | nombretipocanal | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | banderadocumentodigital | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | banderamercadotecnia | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | fecharegistro | 1 |  |  |  |  |  |  |
|  | 3 | Cloudera kio |  | cu\_bdekt | cu\_deyde\_vwdatainfo\_clienteanonimo\_nombre | IDE | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | IdentificadorDocumento | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | FcNumeroEconomico | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | FCTipoCanalID | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteNombre | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteNombreNexo | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteApellidoPaterno | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteApellidoNexos | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteApellidoMaterno | 0 |  |  |  |  |  |  |
|  | 4 | Cloudera kio |  | cu\_bdekt | cu\_deyde\_vwdatainfo\_clienteanonimo\_correo | IDE | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | IdentificadorDocumento | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | FcNumeroEconomico | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | FCTipoCanalID | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | dir\_ema | 0 |  |  |  |  |  |  |
|  | 5 | Cloudera kio |  | cu\_bdekt | cu\_deyde\_vwdatainfo\_clienteanonimo\_telefono | IDE | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | IdentificadorDocumento | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | FcNumeroEconomico | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | FCTipoCanalID | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | numtel1 | 0 |  |  |  |  |  |  |
|  | 6 | Cloudera kio |  | cu\_baz\_bdclientes | cu\_ta\_frecuencia\_email | dir\_email | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | frecuencia | 0 |  |  |  |  |  |  |
|  | 7 | Cloudera kio |  | cu\_baz\_bdclientes | cu\_baz\_bdclientes.cu\_ta\_frecuencia\_tel1 | indtip1 | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | tel1\_norm | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | frecuencia | 0 |  |  |  |  |  |  |
|  | 8 | Cloudera kio |  | cd\_baz\_bdclientes | cd\_cte\_datos\_contacto\_master | id\_master | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | nexos\_apellido\_paterno | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | apellido\_paterno\_norm | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | nexos\_apellido\_materno | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | apellido\_materno\_norm | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | nombre\_norm | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | tel1\_norm | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | tel2\_norm | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | dir\_email | 0 |  |  |  |  |  |  |
|  | 9 | Cloudera KIO |  | cd\_baz\_bdclientes | cd\_cte\_master | id\_master | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | id\_cliente | 2 |  |  |  |  |  |  |
|  | 10 | Cloudera KIO |  | rd\_baz\_bdclientes | rd\_MCDT403 | t403\_num\_clte | 1 |  |  |  |  |  |  |
|  | 11 | Cloudera KIO |  | cd\_ baz\_bdclientes | cd\_cap\_cuenta\_sem | id\_master | 1 |  | B |  | B |  | B |
|  |  |  |  |  |  | cod estatus | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | cod\_titular | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | cod\_producto | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | cod\_subprod | 0 |  |  |  |  |  |  |
|  | 12 | Cloudera KIO |  | cu\_gs\_bosopoperlog | cu\_ebx\_catm\_gs\_productos\_captacion\_niveles | fcnuevo\_producto\_nivel\_03 | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fcnuevo\_producto\_nivel\_04 | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fcnuevo\_producto\_nivel\_05 | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fccodigo\_subproducto | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | fccodigo\_producto | 1 |  |  |  |  |  |  |
|  | 13 | Cloudera kio |  | cu\_gs\_bdsopoperlog | cu\_ebx\_catm\_gs\_fitires\_niveles | fccredimax\_fitir | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | fcnivel\_1 | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fcnivel\_2 | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fcnivel\_3 | 0 |  |  |  |  |  |  |
|  | 14 | Cloudera KIO |  | cd\_baz\_bdclientes | cd\_cre\_detalle\_pedido | id\_master | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | id\_cliente | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | est\_pedido | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | ind\_credventagestora | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ind\_reasignacion | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fec\_liquidacion | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fec\_cancelacion | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | cod\_fiti | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fccredimax\_fitir | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | id\_pedido\_pais | 0 |  |  |  |  |  |  |
|  | 15 | Cloudera KIO |  | cd\_baz\_bdclientes | cd\_cte\_empleado\_master | id\_master | 1 |  |  |  |  |  |  |
|  | 16 | Cloudera KIO |  | cd\_baz\_bdclientes | cd\_con\_cte\_actividad\_mes | id\_master | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | ind\_activo | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | Num\_Periodo\_mes | 0 |  |  |  |  |  |  |

## 04_CD_Relacion_TBLS_RAW
| : 0 | Crystal Data Relación de Tablas RAW | : 2 | : 3 |
| --- | --- | --- | --- |
|  |  |  |  |
|  | Relación de Tablas RAW es decir Insumos que se requieren para la construcción cd\_ekt\_persona\_envio |  |  |
|  | Paso 1 |  |  |
|  | Descripción | Cruce con información del pedido |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cd\_ekt\_prospecto\_cte\_presupuesto |  |
|  | Tabla B: |  |  |
|  | Relación: |  |  |
|  | Tipo de Unión: |  |  |
|  | Columnas Finales | tiendaID, presupuestoID<br>, max(esPedido) esPedido, <br>, max(B.ClienteUnico) ClienteUnicoPedido,<br>, if(max(TipoVentaID = 2),1,0) as EsPptoCredito |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio | Agrupar por los campos tiendaID, presupuestoID |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_anonimato\_persona\_ppto |  |
|  |  |  |  |
|  | Paso 2 |  |  |
|  | Descripción | Tabla temporal con los Tickets Presupuestos de red única y datos de personas |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cu\_bdekt.cu\_ekt\_cte\_prospecto |  |
|  | Relación: |  |  |
|  | Tipo de Unión: |  |  |
|  | Columnas Finales | cast (ROW\_NUMBER() over (order by numeroeconomicosucursal, documentoid, tipocanalid) as string) as id <br>, numeroeconomicosucursal, documentoid, tipocanalid<br>, nombretipocanal , banderadocumentodigital, banderamercadotecnia, fecharegistro |  |
|  | Filtro y/o condiciones | TipoTicketID = 1 <br>PaisId = 1 <br>NombreDocumento = "Presupuesto"<br>cast(NumeroEconomicoSucursal as int) > 99<br>DocumentoID not in ("0","") and length(DocumentoID) !=19(<br>( clientecorreo not like '%"%' | clientecorreo is null) |  |
|  | Reglas negocio | No se filtra por fecha ya que la estandarización express solo contempla los filtros indicados en este paso |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_anonimato\_persona |  |
|  |  |  |  |
|  | Paso 3 |  |  |
|  | Descripción | Tabla temporal con los Tickets Presupuestos de red única |  |
|  | Origen Tablas Temporales | Paso 1 y Paso 2 |  |
|  | Tabla A: | TEMP\_anonimato\_persona\_ppto |  |
|  | Tabla B: | TEMP\_anonimato\_persona |  |
|  | Relación: | A.tiendaID = B.numeroeconomicosucursal<br>A.presupuestoID = B.documentoid |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | Distinct A.tiendaID, A.presupuestoID, A.esPedido, A.ClienteUnicoPedido, A.EsPptoCredito<br>B.id, B.tipocanalid, B.nombretipocanal , B.banderadocumentodigital, B.banderamercadotecnia, B.fecharegistro |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_base\_persona |  |
|  |  |  |  |
|  |  |  |  |
|  | Paso 4 |  |  |
|  | Descripción | Tabla Temporal aplicando criterios de calidad de laestandarización expres |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cu\_bdekt.cu\_deyde\_vwdatainfo\_clienteanonimo\_nombre |  |
|  | Tabla B: | cu\_bdekt.cu\_deyde\_vwdatainfo\_clienteanonimo\_correo |  |
|  | Relación: | A.ide=B.ide and B.fitipocanalenvid=2 |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid<br> , if( (dir\_ema='3' and fs\_ema='9') or (dir\_ema='2' and fs\_ema='7'),1,0) marcaCorreo<br> , concat\_ws(' ',descencriptar(A.nombre), A.nexos1, descencriptar(A.apell1), A.nexos2 ,descencriptar(A.apell2)) AS nombrecompleto\_norm, ,A.nombre, A.nexos1, A.apell1, A.nexos2, A.apell2<br> , dd\_ema, fd\_ema, fs\_ema, dir\_ema<br> , descencriptar(dd\_ema) dir\_email<br> , if( fd\_ema.isin('B','F') ,0, Cast( fd\_ema as int)) as indema<br> , if( fs\_ema = 'B' and fd\_ema = 'B',0,1) as EMA\_COMP\_NULO<br> , if( fs\_ema = 'F' and fd\_ema = 'F',0,1) as EMA\_COMP\_FICT<br> , if( fs\_ema in ('0', '2') and fd\_ema in ('0', '3', '7', '6'), 0, 1) as EMA\_CONF\_SINT <br> , if( fs\_ema = '0' and fd\_ema in ('0', '3', '7', '6'), 0, 1) as EMA\_PREC\_DOMI <br> , if( fs\_ema = '0' and fd\_ema in ('3', '7'), 0, 1) as EMA\_REME\_SINT<br> , if( fs\_ema = '0' and fd\_ema in ('6', '8'), 0, 1) as EMA\_REME\_DOMI<br> , if( substr( dd\_ema,instr( descencriptar(dd\_ema) ,'@')+ 1) in ('gmail.com', 'hotmail.com', 'outlook.com','yahoo.com.mx', 'live.com.mx', 'yahoo.com', 'live.com', 'hotmail.es', 'prodigy.net.mx', 'msn.com', 'outlook.es', 'icloud.com', 'yahoo.es','onewaymail.com', 'latinmail.com', 'terrD.com.mx', 'aol.com', 'facebook.com', 'rocketmail.com', 'itelcel.com', 'bbvD.com', 'pemex.com','live.com.ar', 'comunidad.unam.mx', 'imss.gob.mx', 'cfe.gob.mx', 'telmexmail.com', 'inegi.org.mx', 'hotmail.com.ar', 'banorte.com','yahoo.fr', 'ciencias.unam.mx', 'cablevision.net.mx', 'uabc.edu.mx', 'ipn.mx'), 1, 0) as EMA\_PREC\_CATA |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_NFR\_CORREO |  |
|  |  |  |  |
|  | Paso 5 |  |  |
|  | Descripción | Cruce temporal con la frecuencia del número del correo |  |
|  | Origen Tablas Temporales | Paso 4 |  |
|  | Tabla A: | TEMP\_NFR\_CORREO |  |
|  | Tabla B: | cu\_baz\_bdclientes.cu\_ta\_frecuencia\_email |  |
|  | Relación: | A.dir\_email = B.dir\_email |  |
|  | Tipo de Unión: | Left join |  |
|  | Columnas Finales | ide, fcnumeroeconomico, identificadordocumento, fitipocanalenvid<br> , dd\_ema, fs\_ema, dir\_ema<br> , marca\_correo, nombrecompleto\_norm, nombre, nexos1, apell1, nexos2, apell2<br> , 1 as id\_delta<br> , CASE WHEN A.dd\_ema IS NULL or A.dd\_ema = '' THEN 0 WHEN B.frecuencia >= 10 THEN 0 ELSE 1 END EMA\_DUPL\_REPT<br> , CASE WHEN A.fd\_ema in ( 'B' , 'F') THEN 0 ELSE CAST(A.fd\_ema AS INT) END indema<br> , A.EMA\_COMP\_NULO<br> , A.EMA\_COMP\_FICT<br> , A.EMA\_CONF\_SINT<br> , A.EMA\_PREC\_DOMI<br> , A.EMA\_REME\_SINT<br> , A.EMA\_REME\_DOMI<br> , A.EMA\_PREC\_CATA<br>  , dir\_email<br> |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_FREUENCIA\_CORREO |  |
|  |  |  |  |
|  | Paso 6 |  |  |
|  | Descripción | Generación de tabla temporal con los correos y su calificación de la estandarización |  |
|  | Origen Tablas Temporales | Paso 5 |  |
|  | Tabla A: | TEMP\_FREUENCIA\_CORREO |  |
|  | Relación: |  |  |
|  | Tipo de Unión: |  |  |
|  | Columnas Finales | IDE, fcnumeroeconomico, identificadordocumento, fitipocanalenvid, dir\_email, dd\_ema<br> , Round(((indema \* 0.05 + greatest(0,1 - (1 - EMA\_COMP\_NULO) - (1 - EMA\_COMP\_FICT) - 0.5 \* (1 - EMA\_CONF\_SINT) - 0.5 \* (1 - EMA\_PREC\_DOMI) - 0.1 \* (1 - EMA\_REME\_SINT) - 0.1 \* (1 - EMA\_REME\_DOMI) - 0.75 \* (1 - EMA\_DUPL\_REPT) - 0.4 \* (1- EMA\_PREC\_CATA)) \* 0.5)),4) as ICN\_EMAIL<br>, case when Round(((indema \* 0.05 + greatest(0,1 - (1 - EMA\_COMP\_NULO) - (1 - EMA\_COMP\_FICT) - 0.5 \* (1 - EMA\_CONF\_SINT) - 0.5 \* (1 - EMA\_PREC\_DOMI) - 0.1 \* (1 - EMA\_REME\_SINT) - 0.1 \* (1 - EMA\_REME\_DOMI) - 0.75 \* (1 - EMA\_DUPL\_REPT) - 0.4 \* (1- EMA\_PREC\_CATA)) \* 0.5)),4) < 0.50 then '5.Nulo' when Round(((indema \* 0.05 + greatest(0,1 - (1 - EMA\_COMP\_NULO) - (1 - EMA\_COMP\_FICT) - 0.5 \* (1 - EMA\_CONF\_SINT) - 0.5 \* (1 - EMA\_PREC\_DOMI) - 0.1 \* (1 - EMA\_REME\_SINT) - 0.1 \* (1 - EMA\_REME\_DOMI) - 0.75 \* (1 - EMA\_DUPL\_REPT) - 0.4 \* (1- EMA\_PREC\_CATA)) \* 0.5)),4) < 0.70 then '4.Malo' twhen Round(((indema \* 0.05 + greatest(0,1 - (1 - EMA\_COMP\_NULO) - (1 - EMA\_COMP\_FICT) - 0.5 \* (1 - EMA\_CONF\_SINT) - 0.5 \* (1 - EMA\_PREC\_DOMI) - 0.1 \* (1 - EMA\_REME\_SINT) - 0.1 \* (1 - EMA\_REME\_DOMI) - 0.75 \* (1 - EMA\_DUPL\_REPT) - 0.4 \* (1- EMA\_PREC\_CATA)) \* 0.5)),4) < 0.85 then '3.Regular' else '2.Bueno' end as ICC\_EMAIL<br>, IF( (ICC\_EMAIL == '3.Regular') and marca\_correo = 1 and trim(nombrecompleto\_norm) not in (' ','') and trim(dir\_email)!="" , 1, 0) FlagCorreo<br>, nombre, nexos1, apell1, nexos2, apell2, nombrecompleto\_norm |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_CORREO |  |
|  |  |  |  |
|  | Paso 7 |  |  |
|  | Descripción | Tabla Temporal aplicando criterios de calidad de la estandarización express para número de teléfono |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cu\_bdekt.cu\_deyde\_vwdatainfo\_clienteanonimo\_nombre |  |
|  | Tabla B: | cu\_bdekt.cu\_deyde\_vwdatainfo\_clienteanonimo\_telefono |  |
|  | Relación: | A.ide=B.ide and and B.fitipocanalenvid!=2 |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid<br>IF(B.indtel1 IS NULL AND B.indver1 IS NULL,0, IF(B.indtel1 = '0' AND B.indver1 IN('0','1'),0,1)) AS CEL\_COMP\_NULO , <br> IF(descencriptar(numtel1) ='' OR descencriptar(numtel1) IS NULL,0, IF (LENGTH(B.numtel1) = 10,1,0)) AS CEL\_CONF\_LONG , <br> IF(B.indtel1 IS NULL AND B.indver1 IS NULL,0, IF (B.indtel1 = '5' AND B.indver1 = '6',0,1)) AS CEL\_PREC\_NOTE , <br> IF(B.indtel1 IS NULL AND B.indver1 IS NULL,0, IF (B.indtel1 = '2' AND B.indver1 IN ('2','3','4','5'),0,1)) AS CEL\_REME\_LAAC , <br> IF(descencriptar(B.numtel1) IS NULL OR descencriptar(B.numtel1) = '',0, IF( descencriptar(B.numtel1) LIKE'%01234%' OR descencriptar(B.numtel1) LIKE'%12345%' OR descencriptar(B.numtel1) LIKE'%23456%' OR descencriptar(B.numtel1) LIKE'%34567%' OR descencriptar(B.numtel1) LIKE '%45678%' OR descencriptar(B.numtel1) LIKE'%56789%',0,1)) AS CEL\_VALI\_SECU , <br> IF(descencriptar(B.numtel1) IS NULL OR A.descencriptar(B.numtel1) ='',0, IF.descencriptar(B.numtel1) LIKE'%00000%',0,1)) AS CEL\_VALI\_CERO , <br> IF(descencriptar(B.numtel1) IS NULL OR descencriptar(B.numtel1) ='',0, IF(descencriptar(B.numtel1) = REGEXP\_REPLACE(descencriptar(B.numtel1) ,'[^0-9]','0'),1,0)) AS CEL\_CONF\_NUME , <br> B.numtel1 , B.indtip1 , B.indtel1 ,B.indvar1<br>, descencriptar(B.numtel1) celular1<br>, concat\_ws(' ',descencriptar(A.nombre), A.nexos1, descencriptar(A.apell1), nexos2 ,descencriptar(A.apell2)) AS nombrecompleto\_norm, A.nombre, A.nexos1, A.apell1, A.nexos2, A.apell2<br>IF( ( (indtel1='2' and indver1='2') OR (indtel1='2' and indver1='3') OR (indtel1='4' and indver1='7')),1,0) MarcaCelular<br> |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_NFR\_CELULAR |  |
|  |  |  |  |
|  | Paso 8 |  |  |
|  | Descripción | Cruce temporal con la frecuencia del número del celular |  |
|  | Origen Tablas Temporales | Paso 7 |  |
|  | Tabla A: | TEMP\_NFR\_CELULAR |  |
|  | Tabla B: | cu\_baz\_bdclientes.cu\_ta\_frecuencia\_tel1 |  |
|  | Relación: | A.numtel1 = B.tel1\_norm AND A.indtip1 = B.indtip1 |  |
|  | Tipo de Unión: | Left join |  |
|  | Columnas Finales | A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid<br>, 1 AS id\_delta <br> ,CASE WHEN celular1 or celular1= '' THEN 0 WHEN B.frecuencia IS NOT NULL THEN CASE WHEN A.indtip1 = 'M' then IF(B.frecuencia >=4,0,1) WHEN A.indtip1 = 'F' then IF(B.frecuencia >=7,0,1) ELSE 1 END ELSE 1 END CEL\_DUPL\_REPT <br> , CEL\_COMP\_NULO <br> , CEL\_CONF\_LONG <br> , CEL\_CONF\_NUME <br> , CEL\_REME\_LAAC <br> , CEL\_PREC\_NOTE <br> , CEL\_VALI\_SECU <br> , CEL\_VALI\_CERO <br> ,A.numtel1 <br> ,A.indtip1 <br> ,A.ndtel1 ,indvar1, celular1<br>, MarcaCelular , nombre, nexos1, apell1, nexos2, apell2, nombrecompleto\_norm<br> |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_FREUENCIA\_CELULAR |  |
|  |  |  |  |
|  | Paso 9 |  |  |
|  | Descripción | Generación de tabla temporal con los correos y su calificación de la estandarización |  |
|  | Origen Tablas Temporales | Paso 8 |  |
|  | Tabla A: | TEMP\_FREUENCIA\_CELULAR |  |
|  | Relación: |  |  |
|  | Tipo de Unión: |  |  |
|  | Columnas Finales | A.numtel1 ,A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid , celular1, <br>, Round(((cASt(A.indtel1 AS INT) \* 0.05 + GREATEST(0,1 - (1 - A.CEL\_COMP\_NULO) - 0.5 \* (1 - A.CEL\_CONF\_LONG) - 0.5 \* (1 - A.CEL\_CONF\_NUME) - 0.75 \* (1 - A.CEL\_DUPL\_REPT)- 0.25 \* (1 - A.CEL\_REME\_LAAC) - 0.10 \*(1 - A.CEL\_PREC\_NOTE) - 0.5 \* (1 - A.CEL\_VALI\_SECU) - 0.5 \* (1 - A.CEL\_VALI\_CERO)) \* 0.5)),4) AS ICN\_CELULAR <br>,CASE WHEN ROUND(((cASt(A.indtel1 AS INT) \* 0.05 + GREATEST(0,1 - (1 - A.CEL\_COMP\_NULO) - 0.5 \* (1 - A.CEL\_CONF\_LONG) - 0.5 \* (1 - A.CEL\_CONF\_NUME) - 0.75 \* (1 - A.CEL\_DUPL\_REPT)- 0.25 \* (1 - A.CEL\_REME\_LAAC) - 0.10 \* (1 - A.CEL\_PREC\_NOTE) - 0.5 \* (1 - A.CEL\_VALI\_SECU) - 0.5 \* (1 - A.CEL\_VALI\_CERO)) \* 0.5)),4) < 0.5 THEN '5.Nulo' <br>WHEN ROUND(((cASt(A.indtel1 AS INT) \* 0.05 + GREATEST(0,1 - (1 - A.CEL\_COMP\_NULO) - 0.5 \* (1 - A.CEL\_CONF\_LONG) - 0.5 \* (1 - A.CEL\_CONF\_NUME) - 0.75 \* (1 - A.CEL\_DUPL\_REPT)- 0.25 \* (1 - A.CEL\_REME\_LAAC) - 0.10 \* (1 - A.CEL\_PREC\_NOTE) - 0.5 \* (1 - A.CEL\_VALI\_SECU) - 0.5 \* (1 - A.CEL\_VALI\_CERO)) \* 0.5)),4) < 0.70 THEN '4.Malo' <br>WHEN ROUND(((cASt(A.indtel1 AS INT) \* 0.05 + GREATEST(0,1 - (1 - A.CEL\_COMP\_NULO) - 0.5 \* (1 - A.CEL\_CONF\_LONG) - 0.5 \* (1 - A.CEL\_CONF\_NUME) - 0.75 \* (1 - A.CEL\_DUPL\_REPT)- 0.25 \* (1 - A.CEL\_REME\_LAAC) - 0.10 \* (1 - A.CEL\_PREC\_NOTE) - 0.5 \* (1 - A.CEL\_VALI\_SECU) - 0.5 \* (1 - A.CEL\_VALI\_CERO)) \* 0.5)),4) < 0.85 THEN '3.Regular' <br>ELSE '2.Bueno' END AS ICC\_CELULAR <br>, IF( ( ICC\_CELULAR == '3.Regular') and (MarcaCelular = 1) and trim(nombrecompleto\_norm) not in (' ','') and trim(celular1)!="", 1, 0) FlagCelular<br>, nombre, nexos1, apell1, nexos2, apell2, nombrecompleto\_norm |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_CELULAR |  |
|  |  |  |  |
|  | Paso 10 |  |  |
|  | Descripción | Tabla temporal para la frecuencia del correo |  |
|  | Origen Tablas Temporales | Paso 9 y Paso 6 |  |
|  | Tabla A: | TEMP\_CORREO |  |
|  | Tabla B: | TEMP\_CELULAR |  |
|  | Relación: | A.ide=B.ide <br>and A.fcnumeroeconomico= B.fcnumeroeconomico and A.identificadordocumento = B.identificadordocumento and A.fitipocanalenvid = B.fitipocanalenvid |  |
|  | Tipo de Unión: | UNION |  |
|  | Columnas Finales | ( A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid <br>, A.nombre ClienteNombre, A.nexos1 ClienteNombreNexo, A.apell1 ClienteApellidoPaterno, A.nexos2 ClienteApellidoNexos, A.apell2 ClienteApellidoMaterno<br>, A.nombrecompleto\_norm<br>, A.dd\_ema ClienteCorreo, A.ICN\_EMAIL ClienteIndicadorCorreo, A.ICC\_EMAIL ClienteCalificaciónCorreo, A.FlagCorreo, A.dir\_email<br>, "N/A" as ClienteCelular, -1.0 ClienteIndicadorCelular, "5.Nulo" ClienteCalifcacionCelular, 0 FlagCelular, "N/A" celular1)<br>union all <br>( B.ide, B.fcnumeroeconomico, B.identificadordocumento, B.fitipocanalenvid <br>, B.nombre ClienteNombre, B.nexos1 ClienteNombreNexo, B.apell1 ClienteApellidoPaterno, B.nexos2 ClienteApellidoNexos, B.apell2 ClienteApellidoMaterno, B.nombrecompleto\_norm<br>, "N/A" as ClienteCorreo, -1.0 ClienteIndicadorCorreo, "5.Nulo" as ClienteCalificacionCorreo, 0 FlagCorreo, "N/A" as dir\_email<br>, B.numtel1 ClienteCelular, B.ICN\_CELULAR ClienteIndicadorCelular, B.ICC\_CELULAR ClienteCalifcaciónCelular, B.FlagCelular, B.celular1) |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_BASE\_EXT |  |
|  |  |  |  |
|  | Paso 11 |  |  |
|  | Descripción | Tabla temporal para la generación de MasterID para cruzar de acuerdo al cliente único |  |
|  | Origen Tablas Temporales | Paso 10 |  |
|  | Tabla A: | TEMP\_BASE\_EXT |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_cte\_datos\_contacto\_master |  |
|  | Relación: | A.dir\_email = B.dir\_email <br> trim(A.nombrecompleto\_norm),<br> trim( concat\_ws(' ',B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm) ) <br> ) >= 90 ) <br>trim(concat\_ws(' ', B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm)) not in (' ','') |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid , B.id\_master |  |
|  | Filtro y/o condiciones | FlagCorreo = 1 |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_NOMBRE\_CORREO |  |
|  |  |  |  |
|  | Paso 12 |  |  |
|  | Descripción | Tabla temporal para la generación de MasterID para cruzar de acuerdo al cliente único |  |
|  | Origen Tablas Temporales | Paso 10 |  |
|  | Tabla A: | TEMP\_BASE\_EXT |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_cte\_datos\_contacto\_master |  |
|  | Relación: | (B.tel1\_norm = A.celular1) & (B.tel1\_norm!='5555555555')<br>(100 - LEVENSHTEIN(<br> trim(A.nombrecompleto\_norm),<br> trim( concat\_ws(' ',B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm) ) <br> ) >= 90 )<br>trim(concat\_ws(' ', B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm)) not in (' ','') |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid , B.id\_master |  |
|  | Filtro y/o condiciones | FlagCelular = 1 |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_NOMBRE\_TELEFONO1 |  |
|  |  |  |  |
|  | Paso 13 |  |  |
|  | Descripción | Tabla temporal para la generación de MasterID para cruzar de acuerdo al cliente único |  |
|  | Origen Tablas Temporales | Paso 10 |  |
|  | Tabla A: | TEMP\_BASE\_EXT |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_cte\_datos\_contacto\_master |  |
|  | Relación: | (B.tel2\_norm = A.celular1) & (B.tel2\_norm !='5555555555')<br>(100 - LEVENSHTEIN(<br> trim(A.nombrecompleto\_norm),<br> trim( concat\_ws(' ',B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm) ) <br> ) >= 90 )<br>trim(concat\_ws(' ', B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm)) not in (' ','') |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid , B.id\_master |  |
|  | Filtro y/o condiciones | FlagCelular = 1 |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_NOMBRE\_TELEFONO2 |  |
|  |  |  |  |
|  | Paso 14 |  |  |
|  | Descripción | Relación temporal con el ID\_Master por coincidencia de teléfono ocorreo |  |
|  | Origen Tablas Temporales | Paso 11, Paso 12 Y Paso 13 |  |
|  | Tabla A: | TEMP\_RELACION\_NOMBRE\_CORREO |  |
|  | Tabla B: | TEMP\_RELACION\_NOMBRE\_TELEFONO1 |  |
|  | Tabla B: | TEMP\_RELACION\_NOMBRE\_TELEFONO2 |  |
|  | Relación: |  |  |
|  | Tipo de Unión: | UNION |  |
|  | Columnas Finales | select \* from relacion\_nombre\_telefono1<br> union<br> select \* from relacion\_nombre\_telefono2<br> union<br> select \* from relacion\_nombre\_correo |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  |  |  |  |
|  | Paso 15 |  |  |
|  | Descripción | Tabla temporal para la generación de MasterID para cruzar de acuerdo al cliente único |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cd\_baz\_bdclientes.cd\_cte\_master |  |
|  | Relación: |  |  |
|  | Tipo de Unión: |  |  |
|  | Columnas Finales | min(id\_master) as id\_master,<br> id\_cliente as ClienteUnico |  |
|  | Filtro y/o condiciones | Obtener el minimo del ID\_Master<br>cod\_tipo\_cliente='CLIENTE\_UNICO' |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_MasterID\_1 |  |
|  |  |  |  |
|  | Paso 16 |  |  |
|  | Descripción | Generación de tabla temporal con el cliente unico |  |
|  | Origen Tablas Temporales | Paso 14 y Paso 15 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla B: | TEMP\_MasterID\_1 |  |
|  | Relación: | A. id\_master = B. id\_master |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | distinct A.id\_master, B.ClienteUnico |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_CU |  |
|  |  |  |  |
|  | Paso 17 |  |  |
|  | Descripción | Identificación si es digital |  |
|  | Origen Tablas Temporales | Paso 16 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID\_CU |  |
|  | Tabla B: | rd\_baz\_bdclientes.rd\_MCDT403 |  |
|  | Relación: | A.ClienteUnico = B.t403\_num\_clte |  |
|  | Tipo de Unión: | left join |  |
|  | Columnas Finales | A.id\_master, <br>collect\_set(ClienteUnico) ClienteUnico<br>max(case when A.id\_master is not null and A.ClienteUnico is not null then 1 else 0 end) marcaProceso<br>max(case when B.t403\_num\_clte is not null then 1 else 0 end) esDigital |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_DIGITAL |  |
|  |  |  |  |
|  | Paso 18 |  |  |
|  | Descripción | Adición del Crystal de Crédito |  |
|  | Origen Tablas Temporales | Paso 14 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla B: | cd\_ baz\_bdclientes.cd\_cap\_cuenta\_sem |  |
|  | Tabla C: | cu\_gs\_bosopoperlog.cu\_ebx\_catm\_gs\_productos\_captacion\_niveles |  |
|  | Relación: | A.id\_master = B.id\_master<br>B.cod\_producto = C.fccodigo\_producto AND B.cod\_subprod = C. fccodigo\_subproducto<br>AND B.COD\_TITULAR = 'T' and B.cod estatus = "'ACTIVA"<br>AND UPPER (C.fcnuevo\_producto\_nivel\_03) like "%CAPTACION%"<br>AND (UPPER(C.fcnuevo\_producto\_nivel\_04) like "%INVERSION%" OR UPPER(C.fcnuevo\_producto\_nivel\_05) like "%DEBIT0%" OR UPPER(C.fcnuevo\_producto\_nivel\_05) like "%GUARDADIT0%") |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT Aid\_master |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_CAPTA |  |
|  |  |  |  |
|  | Paso 19 |  |  |
|  | Descripción | Adición del Crystal de Crédito |  |
|  | Origen Tablas Temporales | Paso 14 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_cre\_detalle\_pedido |  |
|  | Tabla C: | cu\_gs\_bdsopoperlog.cu\_ebx\_catm\_gs\_fitires\_niveles |  |
|  | Relación: | A.id\_master = B.id\_master<br>B.id\_cliente is not null and B.id\_cliente != ''<br>B.cod\_fitir = cast(C.fccredimax\_fitir as int)<br>B.id\_pedido\_pais = 1<br>B.est\_pedido = 1 and B.ind\_credventagestora = 0 and B.ind\_reasignacion = 0<br>coalesce(B.fec\_liquidacion, B.fec\_cancelacion) is null<br>( trim(C.fcnivel\_1) in ('Prestamos Conectividad', 'Prestamos Hogar', 'Prestamos Italika', 'Prestamos Movilidad') or trim(C.fcnivel\_2) in ('Prestamos Efectivo') or trim(C.fcnivel\_3) in ('Tarjeta Azteca') ) |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT Aid\_master |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_CRYSTAL\_CREDITO |  |
|  |  |  |  |
|  | Paso 20 |  |  |
|  | Descripción | Identificación si es empleado |  |
|  | Origen Tablas Temporales | Paso 14 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_cte\_empleado\_master |  |
|  | Relación: | A.id\_master = B.id\_master<br>B.fc\_status = "ACTIVO" |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT Aid\_master |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_EMPLEADO |  |
|  |  |  |  |
|  | Paso 21 |  |  |
|  | Descripción | Identificación mes anterior |  |
|  | Origen Tablas Temporales | Paso 2 |  |
|  | Tabla A: | TEMP\_anonimato\_persona |  |
|  | Columnas Finales | cast( date\_format( add\_months( from\_unixtime( cast( max(fecharegistro)/1000 as Bigint) , "yyyy-MM-dd" ), -1 ) , "yyyyMM") as int) Num\_Periodo\_mes |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_ANTERIOR\_MES |  |
|  |  |  |  |
|  | Paso 22 |  |  |
|  | Descripción | Identificación si es Activo |  |
|  | Origen Tablas Temporales | Paso 14 y 21 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_con\_cte\_actividad\_mes |  |
|  | Tabla C: | TEMP\_ANTERIOR\_MES |  |
|  | Relación: | A.id\_master = B.id\_master<br>B.ind\_activo = 1 <br>B.Num\_Periodo\_mes = C.Num\_Periodo\_mes |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT A.id\_master |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_ACTIVO |  |
|  |  |  |  |
|  | Paso 23 |  |  |
|  | Descripción | Adición de marca a nivel MasterID |  |
|  | Origen Tablas Temporales | Paso 17, Paso 18, Paso 19, Paso 20 y Paso 22 |  |
| TEMP\_RELACION\_PERSONA\_MASTERID | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID\_DIGITAL |  |
|  | Tabla B: | TEMP\_RELACION\_PERSONA\_MASTERID\_CAPTA |  |
|  | Tabla C: | TEMP\_RELACION\_PERSONA\_MASTERID\_CRYSTAL\_CREDITO |  |
|  | Tabla D: | TEMP\_RELACION\_PERSONA\_MASTERID\_EMPLEADO |  |
|  | Tabla E: | TEMP\_RELACION\_PERSONA\_MASTERID\_ACTIVO |  |
|  | Relación: | A.id\_master = B.id\_master<br>A.id\_master = C.id\_master<br>A.id\_master = D.id\_master<br>A.id\_master = E.id\_master |  |
|  | Tipo de Unión: | Left join |  |
|  | Columnas Finales | A.id\_master, A.CarcaProceso, A.clienteUnico, A.EsDigital<br> ,if(B.id\_master IS NOT NULL,1,0) as EsCaptacion<br> ,if(D.id\_master IS NOT NULL,1,0) as EsCredito<br> ,if(E.id\_master IS NOT NULL,1,0) as EsActivo<br> ,if(F.id\_master IS NOT NULL,1,0) as EsEmpleado<br> |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_MARCAS\_CLIENTE\_MASTER |  |
|  |  |  |  |
|  | Paso 24 |  |  |
|  | Descripción | Adición del Crystal de Crédito |  |
|  | Origen Tablas Temporales | Paso 10 , Paso 14 y Paso 23 |  |
| TEMP\_RELACION\_PERSONA\_MASTERID | Tabla A: | TEMP\_BASE\_EXT |  |
|  | Tabla B: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla C: | TEMP\_MARCAS\_CLIENTE\_MASTER |  |
|  | Relación: | A.ide = B.ide<br>A.fcnumeroeconomico = B.fcnumeroeconomico and A.identificadordocumento=B.identificadordocumento and A.fitipocanalenvid=B.fitipocanalenvid <br>B.id\_master = C.id\_master |  |
|  | Tipo de Unión: | Left join |  |
|  | Columnas Finales | DISTINCT<br> A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid <br>, A.ClienteNombre, A.ClienteNombreNexo, A.ClienteApellidoPaterno, A.ClienteApellidoNexos, A.ClienteApellidoMaterno<br>, A.nombrecompleto\_norm nombrecompletoNorm<br>, A.ClienteCorreo, A.ClienteIndicadorCorreo, A.ClienteCalificacionCorreo<br>, A.ClienteCelular, A.ClienteIndicadorCelular, A.ClienteCalifcacionCelular<br>, B.id\_master<br>, C.EsCaptacion, C.EsCredito, C.EsDigital, C.EsActivo, C.EsEmpleado, C.MarcaProceso, C.ClienteUnico |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_MARCAS\_CLIENTE |  |
|  |  |  |  |
|  | Paso 25 |  |  |
|  | Descripción | Tabla temporal con las base del Crystal |  |
|  | Origen Tablas Temporales | Paso 3 y Paso 24 |  |
|  | Tabla A: | TEMP\_base\_persona |  |
|  | Tabla B: | TEMP\_MARCAS\_CLIENTE |  |
|  | Relación: | A.tiendaID = B.fcnumeroeconomico, <br>A.presupuestoID = B.identificadordocumento<br>A.tipocanalid = B.fitipocanalenvid |  |
|  | Tipo de Unión: | left join |  |
|  | Columnas Finales | A.tiendaID, A.presupuestoID<br>, A.esPedido, A.ClienteUnicoPedido, A.EsPptoCredito, A.tipocanalid, A.nombretipocanal , A.banderadocumentodigital, A.banderamercadotecnia, Afecharegistro<br>, B.ClienteNombre, B.ClienteNombreNexo, B.ClienteApellidoPaterno, B.ClienteApellidoNexos, B.ClienteApellidoMaterno<br>, B.ClienteCorreo, B.ClienteIndicadorCorreo, B.ClienteCalificacionCorreo<br>, B.ClienteCelular, B.ClienteIndicadorCelular, B.ClienteCalifcacionCelular<br>, B.id\_master MasterID<br>, nvl(B.EsCaptacion,0) as EsCaptacion, nvl(B.EsCredito,0) as EsCredito, nvl(B.EsDigital,0) as EsDigital, nvl(B.esActivo as esActivo), nvl(B.EsEmpleado,0) as EsEmpleado, nvl(B.marcaProceso,0) as marcaProceso, nvl(B.clienteUnico,0) as clienteUnico <br>, if(B.id\_master is not null,1,0) as EsPersonaConocida |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales | fechaRegistro en formato TimeStamps |  |
|  | Tabla Output | TEMP\_cd\_ekt\_prospecto\_cte\_canales\_envio\_previo\_01 |  |
|  |  |  |  |
|  | Paso 26 |  |  |
|  | Descripción | Se actualizan masterid, clienteunico e indicadores |  |
|  | Origen Tablas Temporales | Paso 25, Paso 26.1 |  |
|  | Tabla A: | TEMP\_cd\_ekt\_prospecto\_cte\_canales\_envio\_previo\_01 as cd |  |
|  | Tabla B: | TMP\_ppto as ppto |  |
|  | Tipo de Unión: | left join |  |
|  | Relación: | La relación se realiza por medio de los campos tiendaid y presupuestoid de cada tabla |  |
|  | Columnas Finales: | La selección se realiza de los registos úncos de los siguientes campos<br><br> cd.tiendaid<br>,cd.presupuestoid<br>,espedido<br>,clienteunicopedido<br>,espptocredito<br>,cd.tipocanalid<br>,cd.nombretipocanal<br>,cd.banderadocumentodigital<br>,cd.banderamercadotecnia<br>,cd.fecharegistro<br>,cd.clientenombre<br>,cd.clientenombrenexo<br>,cd.clienteapellidopaterno<br>,cd.clienteapellidonexos<br>,cd.clienteapellidomaterno<br>,cd.clientecorreo<br>,cd.clienteindicadorcorreo<br>,cd.clientecalificacioncorreo<br>,cd.clientecelular<br>,cd.clienteindicadorcelular<br>,cd.clientecalifcacioncelular |  |
|  |  | ,masterid<br>,cd.escaptacion<br>,escredito<br>,cd.esdigital<br>,cd.esactivo<br>,cd.esempleado<br>,cd.marcaproceso<br>,clienteunico<br>,espersonaconocida |  |
|  | Tratamiento campos especiales | Para el espedido, se valida si el campo ppto.espedido es igual a 1, en caso de ser cierto se asigna el valor 1, de lo contrario asigna el valor 0 <br><br>Para el clienteunicopedido, selecciona el campo ppto.clienteunico<br><br>Para el espptocredito, se valida si el campo ppto.ind\_EsPptoCredito es igual a 1, en caso de ser cierto se asigna el valor 1, de lo contrario asigna el valor 0<br><br>Para el masterid, se valida si el campo ppto.masterid es nulo, en caso de ser cierto se asigna el valor 0, de lo contrario selecciona el campo ppto.masterid<br><br>Para el escredito, valida si el ind\_escredito es igual a 1, en caso de ser cierto asigna el valor 1, de lo contrario asigna el valor 0<br><br>Para el clienteunico, valida si el campo ppto.ind\_clienteunico es igual a 1, en caso de ser cierto asigna el valor 1, de lo contrario asigna el valor 0<br><br>Para el espersonaconocida, valida si el campo ppto.masterid es mayor que 0, en caso de ser cierto asigna el valor 1, de lo contrario asigna el valor 0 |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tabla Output | cd\_ekt\_prospecto\_cte\_canales\_envio |  |
|  |  |  |  |
|  | Paso 26.1 |  |  |
|  | Descripción | Se realiza el cruce entre presupuestos únicos y pedidos únicos |  |
|  | Origen Tablas Temporales | Paso 26.1.1, Paso 26.1.2 |  |
|  | Tabla A: | TMP\_ppto1 as ppto1 |  |
|  | Tabla B: | TMP det\_pedido as det\_pedido |  |
|  | Tipo de Unión: | left join |  |
|  | Relación: | La relación se realiza entre el campo ppto1.idpedidounico de la tabla A y el campo det\_pedido.pedido\_unico de la tabla B |  |
|  | Columnas Finales: | La selección se realiza de los registos úncos de los siguientes campos<br><br> ppto1.tiendaid<br>,ppto1.presupuestoid<br>,ppto1.masterid<br>,ppto1.clienteunico<br>,ppto1.idpedidounico<br>,ppto1.espedido<br>,ind\_EsPptoCredito<br>,ind\_clienteunico<br>,ind\_escredito |  |
|  | Tratamiento campos especiales | Para el ind\_EsPptoCredito, se valida si el campo ppto1.tipoventaid es igual a 2, en caso de ser cierto se asigna el valor 1, de lo contrario asigna el valor 0<br><br>Para el ind\_clienteunico, al campo ppto1.clienteunico:<br> Si el valor original es nulo, se asigna el valor de cadena vacía<br> A la cadena resultante, se le quitan los espacios blancos a la derecha y a la izquierda<br> Si la cadena resultante es diferente a cadena vacía, asigna el valor 1, de lo contrario asigna el valor 0<br> <br>Para el ind\_escredito, valida si el campo det\_pedido.pedido\_unico es no nulo, en caso de ser cierto asigna el valor 1, de lo contrario asigna el valor 0 |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tabla Output | TMP\_ppto |  |
|  |  |  |  |
|  | Paso 26.1.1 |  |  |
|  | Descripción | Se obtienen los presupuestos únicos y sus campos principales |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cd\_ekt\_bdclientes.cd\_ekt\_prospecto\_cte\_pesupuesto |  |
|  | Columnas Finales: | La selección se realiza de los registos úncos de los siguientes campos<br><br> tiendaid<br>,presupuestoid<br>,masterid<br>,clienteunico<br>,idpedidounico<br>,espedido<br>,tipoventaid |  |
|  | Tratamiento campos especiales |  |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tabla Output | TMP\_ppto1 |  |
|  |  |  |  |
|  | Paso 26.1.2 |  |  |
|  | Descripción | Se obtienen los pédidos únicos |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cd\_baz\_bdclientes.cd\_cre\_detalle\_pedido |  |
|  | Columnas Finales: | La selección se realiza de los registos úncos de los siguientes campos<br><br>pedido\_unico |  |
|  | Tratamiento campos especiales | Para el pedido\_unico, se realiza: <br> La conversión a cadena del campo id\_pedido\_pais<br> La conversión a cadena del campo id\_pedido\_canal<br> La conversión a cadena del campo id\_pedido\_sucursal<br> La conversión a cadena del campo id\_pedido\_num <br> La concatenación de los campos anteriores, separando con guión medio cada campo |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tabla Output | TMP\_det\_pedido |  |
|  |  |  |  |
|  |  |  |  |
|  | Diccionario de Datos |  |  |
|  | Nombre | Nombre | Nombre |
|  | tiendaID | Número económico que pertenece a la sucursal | String |
|  | presupuestoID | Indica el número de presupuesto o ID al que pertenece el documento | String |
|  | tipocanalid | ID del tipo de canal que realiza el envio | Integer |
|  | nombretipocanal | Nombre del canal en que se realiza el envio | String |
|  | fecharegistro | Fecha en la que se envío el registro | Integer |
|  | MasterID | Indicador de persona a nivel grupo | Integer |
|  | EsPersonaConocida | Marca que permite identificar a la persona | Integer |
|  | EsCaptacion | Indicador si pertenece a la unidad de Captación | Integer |
|  | EsCredito | Indicador si pertenece a la unidad de Crédito y tiene algún pedido | Integer |
|  | EsDigital | Indicador si pertenece a la Digital | Integer |
|  | EsEmpleado | Indicador de pertenecer a empleado | Integer |
|  | esActivo | Indicador si el cliente es activo al momento de consultarse | Integer |
|  | EsPptoCredito | Indicador si el presupuesto es de crédito | Integer |
|  | esPedido | Indicador si el presupuesto se convirtio en pedido | List<String> |
|  | ClienteUnico | Cliente único asociadoMasterID por datos de la persona | Integer |
|  | ClienteUnicoPedido | Cliente único asociado al pedido que compro el cliente por una venta de crédito | Integer |
|  | banderadocumentodigital | Campo que indica la decisión de recibir documentos digitales por el cliente | Integer |
|  | banderamercadotecnia | Campo que indica la decisión de recibir campañas de marketing por el cliente | String |
|  | ClienteNombre | Nombre del cliente | String |
|  | ClienteNombreNexo | Nexoentre los nombres dell Cliente | String |
|  | ClienteApellidoPaterno | Apellido paterno que pertenece al cliente potencial | String |
|  | ClienteApellidoNexos | Nexoentre los nombres dell Cliente | String |
|  | ClienteApellidoMaterno | Apellido materno que pertenece al cliente potencial | String |
|  | ClienteCorreo | Correo electrónico que pertenece al cliente | String |
|  | ClienteIndicadorCorreo | Valor numerico de la calificación del corre del cliente | String |
|  | ClienteCalificaciónCorreo | Calificación de calidad del correo del cliente | String |
|  | ClienteCelular | Número celular que pertenece al cliente | String |
|  | ClienteIndicadorCelular | Valor numerico de la calificación del celular del cliente | String |
|  | ClienteCalifcaciónCelular | Calificación de calidad del celular del cliente |  |

## 05_CD_DER
| : 0 | Crystal Data Diagrama Entidad Relación |
| --- | --- |

## 06_CD_Criterios_de_Aceptación
| : 0 | Criterios de Aceptación | : 2 |
| --- | --- | --- |
|  |  |  |
|  | Criterios de aceptación |  |
|  | No. | Descripción |
|  | 1 | La información se deberá de depositar en esquema de Crystal Data |
|  | 2 | El proceso deberá de tener una peridiocidad a nivel mensual |
|  | 3 | Deberá contemplarse a nivel prospecto |
|  |  |  |
|  |  |  |

## 07_CD_Artefactos
| : 0 | : 1 | : 2 | : 3 | : 4 | : 5 | : 6 |
| --- | --- | --- | --- | --- | --- | --- |
|  | Artefactos |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  | Artefactos |  |  |  |  |  |
|  | No. | Descripción | Responsable | Medio de entrega | Peridiocidad de Entrega | Artefacto |
|  | 1 | Muestra de datos y layout final requerido | DT | Adjunto en este archivo | Única Vez |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  | 2 |  |  |  |  |  |

## 08_CD_Matriz_de_Escalamiento
| : 0 | : 1 | : 2 | : 3 | : 4 | : 5 |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |
|  | Matriz de Escalamiento |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  | Número | Tarea | Aréa | Responsable | Contacto |
|  | 1 | Error en las ingestas | TI | Luis Gerardo Chavez Romero<br>Christopher De Jesus Ochoa Franco | luis.chavezro@elektra.com.mx<br>cochoa@algorithia.com |
|  | 2 | Error en la ejecución del Proceso | TI | Equipo Operaciones | bdfoperaciones@elektra.com.mx |
|  | 3 | Actualización reglas proceso/Error en la consistencia de los datos | Data Translators | Juan Carlos Cifuentes Durán<br>Mauricio Londoño | juan.cifuentesd@algorithia.com<br>mauricio.londonog@algorithia.com |
|  | 4 | Entendimiento de información de Negocio | Negocio | Martin Vega<br>Jose Carlos Montiel | mavega@algorithia.com<br>jose.montielm@algorithia.com |
|  | 5 | Error en datos en tablas RAW | TI Negocio | Alfa Berenice Paredes Flores | abparedes@elektra.com.mx |

## 09_CD_Glosario_de_Términos
| : 0 | : 1 | : 2 |
| --- | --- | --- |
|  |  |  |
|  | Crystal Data Glosario de Términos |  |
|  |  |  |
|  | Glosario |  |
|  | Término | Descripción |

## 10_CD_Linaje
| : 0 | : 1 | : 2 | : 3 | : 4 | : 5 | : 6 | : 7 | : 8 | : 9 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |  |  |  |
|  | Crystal Data Linaje |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |  |
|  | Fuente |  |  |  | Destino |  |  |  |  |
|  | Esquema | Nombre tabla | Nombre de campo | Tipo de dato | Esquema | Nombre tabla | Nombre campo | Tipo de dato | Transformación de campo |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_alta\_pedido\_estatus | id\_tienda | String |  | CU\_ELK\_AGRUPADOVENTA | TiendaID | string |  |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_alta\_pedido\_estatus | id\_tipo\_venta | Inteeger |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer | case <br> when id\_cliente= '99999' THEN 1 <br> when substring(id\_trans\_tb,1,6) in lista\_TEMP\_TAZTOR and (porce\_monto fue con tarjeta TAZ\_TOR) then 2<br> else id\_tipo\_venta <br>end)<br> |
|  |  | TEMP\_TAZTOR | codigo\_bines | String |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer | case <br> when id\_cliente= '99999' THEN 1 <br> when substring(id\_trans\_tb,1,6) in lista\_TEMP\_TAZTOR and (porce\_monto fue con tarjeta TAZ\_TOR) then 2<br> else id\_tipo\_venta <br>end)<br> |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_registra\_pago\_tb | id\_trans\_tb | String |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer | case <br> when id\_cliente= '99999' THEN 1 <br> when substring(id\_trans\_tb,1,6) in lista\_TEMP\_TAZTOR and (porce\_monto fue con tarjeta TAZ\_TOR) then 2<br> else id\_tipo\_venta <br>end)<br> |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_registra\_pago\_tb | monto | Double |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer | case <br> when id\_cliente= '99999' THEN 1 <br> when substring(id\_trans\_tb,1,6) in lista\_TEMP\_TAZTOR and (porce\_monto fue con tarjeta TAZ\_TOR) then 2<br> else id\_tipo\_venta <br>end)<br> |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_registra\_mov\_tipo\_pago | monto | Double |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer | case <br> when id\_cliente= '99999' THEN 1 <br> when substring(id\_trans\_tb,1,6) in lista\_TEMP\_TAZTOR and (porce\_monto fue con tarjeta TAZ\_TOR) then 2<br> else id\_tipo\_venta <br>end)<br> |
|  |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer |  | CU\_ELK\_AGRUPADOVENTA | TipoVenta | String | case when TipoVenta = valordellave then valoroficial end |
|  | cu\_bdsopoperlog | cu\_ebx\_catt\_baz\_tipo\_venta | valordellave | Integer |  | CU\_ELK\_AGRUPADOVENTA | TipoVenta | String | case when TipoVenta = valordellave then valoroficial end |
|  | rd\_baz\_bdclientes | rd\_mon\_201 | valoroficial | String |  | CU\_ELK\_AGRUPADOVENTA | TipoVenta | String | case when TipoVenta = valordellave then valoroficial end |
|  |  | CD\_EKT\_CATALOGO\_SKU | UnidadNegocioID | String |  | CU\_ELK\_AGRUPADOVENTA | DescripcionUnidadNegocio | string | case <br> when UnidadNegocioID in ('1','2','3') <br> then DescripcionUnidadNegocio <br>end |
|  |  | CD\_EKT\_CATALOGO\_SKU | DescripcionUnidadNegocio | String |  | CU\_ELK\_AGRUPADOVENTA | DescripcionUnidadNegocio | string | case <br> when UnidadNegocioID in ('1','2','3') <br> then DescripcionUnidadNegocio <br>end |
|  |  | CD\_EKT\_CATALOGO\_SKU | LineaID | String |  | CU\_ELK\_AGRUPADOVENTA | DescripcionLinea | string | case <br> when LineaID< 900 and LineaID NOT IN (610, 512,560, 770, 760) <br> and SKU.descor not like '%LCR%'<br> then DescripcionLinea <br>end |
|  |  | CD\_EKT\_CATALOGO\_SKU | DescripcionLinea | String |  | CU\_ELK\_AGRUPADOVENTA | DescripcionLinea | string | case <br> when LineaID< 900 and LineaID NOT IN (610, 512,560, 770, 760) <br> and SKU.descor not like '%LCR%'<br> then DescripcionLinea <br>end |
|  |  | CD\_EKT\_CATALOGO\_SKU | DescripcionSublinea | String |  | CU\_ELK\_AGRUPADOVENTA | DescripcionSublinea | string |  |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_detalle\_pedido | cantidad\_venta | double |  | CU\_ELK\_AGRUPADOVENTA | VentaPesos | Double |  |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_detalle\_pedido | cantidad\_articulos | douebl |  | CU\_ELK\_AGRUPADOVENTA | VentaUnidades | Integer |  |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_alta\_pedido\_estatus | fecha\_surtimiento | bigint |  | CU\_ELK\_AGRUPADOVENTA | Anio | string | substring(fecha\_texto(fecha\_surtimiento, "AAAAMMDD"),1,4) |
___
# Microsoft Open Source Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).

Resources:

- [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)
- [Microsoft Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/)
- Contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with questions or concerns
# 📄 **[https://dillinger.io/Politicas Depuración Esquemas Desarrollo.docx](Politicas Depuración Esquemas Desarrollo.docx)** 
___

**Oficina de Gobierno de Datos**

**Febrero 2024**

**Política de Depuración de Tablas en Esquemas de Desarrollo WS - Cloudera**

Índice

1. Control de versiones
2. Descripción de la Política
3. Objetivo de la Política
4. Alcance de la Política
5. Principios de la Política
6. Términos y Definiciones
7. Monitoreo y Cumplimiento
8. Roles y Responsabilidades
9. Autorizadores
10. **Control de Versiones**

El control de versiones nos permite actualizar las políticas y llevar un seguimiento de cada modificación.

| **Versión** | **Fecha** | **Autor** | **Descripción** |
| --- | --- | --- | --- |
| 1.0 | 07 Febrero 2024 | Mario Nonell / Eugenio Salas | Primera Versión de las Políticas de depuración. |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

1. **Descripción de la Política**

La Política de Depuración de tablas en desarrollo en Cloudera establece los lineamientos y procedimientos para identificar, evaluar y eliminar aquellas tablas y esquemas que no cumplan con los estándares y nomenclaturas establecidos por la Oficina de Gobierno de Datos. El objetivo es promover el orden, claridad, consistencia, calidad y eficiencia en la gestión de los datos, además de gestionar el almacenamiento de nuestro Data Lake.

1. **Objetivo de la Política**

Como parte de la gestión de Bases de Datos dentro del Data Lake de Algorithia, es necesario tener consistencia en las nomenclaturas establecidas principalmente en los esquemas (bases de datos) y las tablas, los cuales se construyen según su zona de almacenamiento.

Para tener una plataforma ordenada y funcional, previendo saturación de espacio por procesos que no se ocupan del almacenamiento de los datos, se debe de seguir una política de depuración enfocada a aquellas tablas de desarrollo, la cual se llevará mediante la definición de nomenclaturas de control.

1. **Alcance de la Política**

Esta política se aplica en los ambientes de desarrollo a aquellas tablas temporales, de única ocasión, RFI´s, etc. que no cumplan con los criterios indicados en esta política.

El equipo de OfiGD estará revisando periódicamente el contenido del Data Lake para poder llevar a cabo la depuración en ciertas tablas.

1. **Principios de la Política**

A continuación, se mencionan los principios que rigen nuestra Política de Depuración y que servirán como guía para desarrollar y aplicar esta política.

* ***Cumplimiento de Estándares y Nomenclaturas:*** La depuración de tablas temporales busca garantizar la consistencia del contenido en HUE para tener una gestión de datos ordenada.
* ***Duplicidad:*** No se permite repetir la nomenclatura de una tabla. Si esto sucede, se eliminará la última tabla creada.

Los estándares de nomenclatura definidos son los siguientes y si estos no se cumplen al pie de la letra, se aplicarán las políticas de depuración.

**Nomenclatura para tablas temporales:**

***Tablas de una única ocasión:* os\_empleadoID\_descripcion\_fechacreacion**

**os:** one shot / única ocasión

**empleadoID:** número de empleado

***descripcion:*** descripción breve del contenido del proyecto (Máximo 20 caracteres)

**fechacreacion:** fecha de creación (ddmmaaaa)

**ejemplo:** os\_\_1073861\_cuentas\_16012024

**Regla de depuración:** La tabla se elimina 7 días hábiles después del día de creación.

**Tabla que atiende a solicitud de un RFI: rfi\_folio\_tabla\_fechafin**

**rfi:** solicitud de información

**folio:** folio de la solicitud del RFI, solo se considera la UdN y el consecutivo. (Ejemplo: Captación\_00005)

**fechafin:** fecha fin de la última entrega (ddmmaaaa)

**ejemplo:** rfi\_captacion\_0005\_16012024

**Regla de depuración:** La tabla se elimina 7 días hábiles después del día fin.

**Nota:** En caso de requerir que la tabla no se depure, deben de avisar que antes de que se cumplan los 7 días.

***Tablas Temporal:* tmp\_ empleadoID \_descripcion \_fechafin**

***tmp:*** Tabla temporal

**empleadoID:** número de empleado

***descripcion:*** descripción breve del contenido del proyecto (Máximo 20 caracteres)

**fechafin:** fecha fin compromiso (ddmmaaaa)

***ejemplo:*** tmp\_1073851 \_campanacrm\_10042023

**Nota:** En caso de requerir que la tabla no se depure, deben de avisar antes de que pasen los 15 días de retención en la papelera de depuración.

***Tablas Desarrollo Crystal*: dev\_cd\_udn\_descripcion\_empleadoID**

**dev:** Tabla en desarrollo Crystal

**cd**: Crystal Data

**udn:** Unidad de Negocio a la que pertenece el crystal

***descripcion:*** descripción breve del contenido del proyecto (Máximo 20 caracteres)

**empleadoID:** número de empleado

***ejemplo:*** dev\_cd\_ekt\_saldos\_1073851

**Nota:** Se dara seguimiento puntual con el analítico que solicito la creación de la tabla para validación del avance y confirmación de la depuración una vez que haya sido puesto en producción.

***Tablas Desarrollo Modelo*: dev\_ma\_udn\_descripcion\_empleadoID**

**dev:** Tabla en desarrollo Modelo

**ma:** Modelo Analítico

**udn:** Unidad de Negocio a la que pertenece el crystal

***descripcion:*** descripción breve del contenido del proyecto (Máximo 20 caracteres)

**empleadoID:** número de empleado

***ejemplo:*** dev\_ma\_ekt\_saldos\_1073851

**Nota:** Se dara seguimiento puntual con el analítico que solicito la creación de la tabla para validación del avance y confirmación de la depuración una vez que haya sido puesto en producción.

**Catálogo de UDN**

**baz = Banco Azteca**

**aa = Afore Azteca**

**sa = Seguros Azteca**

**gs = Grupo Salinas**

**ekt = Elektra**

**tp = Total Play**

**faz = Fundación Azteca**

**itk = Italika**

**tva = TV Azteca**

**tn =Tiendas Neto**

1. **Términos y Condiciones**
2. ***Depuración y modificación de tablas temporales***

*a. Nomenclaturas:* Toda tabla temporal debe de seguir las nomenclaturas mencionadas anteriormente, de lo contrario se procede a su depuración, mediante una evaluación mensual en la cual se identifican aquellas tablas que no cumplen con las nomenclaturas definidas.

1. *Periodo de retención:* La retención de las tablas temporales se hará hasta el día que se indique en la nomenclatura **(fechafin).** No se eliminará hasta que la fecha de duración establecida en la nomenclatura lo indique.

b.1. Para las tablas de desarrollo de crystals/modelos, se dará seguimiento puntual con el analítico que solicito la creación de la tabla para validación del avance y confirmación de la depuración una vez que haya sido puesto en producción.

b.2. Las tablas de una única ocasión **(os)** se almacenarán solamente durante 1 semana, por lo que hay que indicar en la nomenclatura, la fecha de creación. **(creación)**

1. Notificación al usuario: Al depurar las tablas temporales se le mandará una notificación al usuario *(es necesario tener el número de empleado en la nomenclatura de la tabla para poder comunicarnos con el usuario),* avisándole que su tabla temporal llego a su fecha de vencimiento.

d.1. Si el usuario necesita seguir trabajando con la tabla en el escritorio virtual, el usuario debe de notificarnos y tenemos un periodo de 15 días a partir de la **(fechafin)**  para regresar la tabla de la Papelera de depuración.

**Condiciones de depuración**

| **Condición** | **Observaciones** | **Caducidad** |
| --- | --- | --- |
| Corrección de Nomenclatura | Al identificar una tabla temporal con la nomenclatura incorrecta o con elementos faltantes como (número de empleado), la tabla procede a su depuración. | Mensualmente se hará una revisión para identificar aquellas tablas que no cumplan con los estándares de nomenclatura y proceder con su depuración. |
| Periodo de retención | Todas las tablas temporales se eliminan automáticamente después de su periodo de retención, al menos que sea una tabla de desarrollo (dev), las cuales pediremos la confirmación del analítico que solicito la creación de la tabla. | El periodo de retención de las tablas temporales se indica en la nomenclatura de la tabla y el de las tablas de desarrollo (dev) se pediremos la confirmación del analítico que solicito la creación de la tabla. |
| Notificación al usuario | Si el usuario necesita seguir trabajando con las tablas temporales y de desarrollo debe de notificar al equipo de Gobierno de Datos para recuperar las tablas de la papelera de depuración. | El usuario tiene 15 días para notificarnos y poder regresarle la tabla de la papelera de depuración y que pueda seguir trabajando. |

1. **Monitoreo y Cumplimiento**

Todas aquellas tablas que no cumplan con las políticas de depuración pasarán al esquema de “Papelera de Depuración” en el cual sólo podrán permanecer hasta 15 días.

\*Definir nomenclatura papelera (genérica o por grupo)

**Papelera de depuración**

Esquema temporal donde se moverán las tablas que se eliminen de los otros esquemas (borrado lógico), con la finalidad de proporcionar un espacio de seguridad durante el proceso de depuración automático, en este espacio se mantendrán las tablas un corto periodo de tiempo (15 días) antes de su borrado definitivo (borrado físico). Cabe aclarar que la papelera de depuración sólo estará visible para los responsables de realizar la depuración.

1. Retención temporal: Las tablas depuradas que no cumplen con las políticas de depuración se enviarán a la papelera de depuración y se retendrán 15 días antes de su eliminación definitiva.
2. Notificación: Cuando una tabla se envía a la papelera de depuración, se enviará una notificación por correo al dueño de la tabla, donde se les informa la fecha de eliminación y la solicitud de requerimiento necesario antes de su eliminación definitiva.
3. Restauración del dueño de la tabla: Durante los 15 días de retención, el dueño de la tabla podrá indicar si la tabla debe de recuperarse o no. Si el dueño decide recuperar la tabla, se restaura en su ubicación original.
4. Eliminación automática: Transcurridos los 15 días de retención en la papelera de depuración, las tablas serán eliminadas automáticamente.
5. **Roles y Responsabilidades**

| **Roles** | **Responsabilidades** |
| --- | --- |
| Data Steward | Responsable de la gestión de los datos y conocimiento del cliente. Este rol es esencial para asegurarse que las tablas del negocio se alineen con los objetivos con los estándares y reglas de integridad de las tablas temporales. |
| Equipo de Gobierno de Datos | Responsables de implementar las políticas de depuración y supervisar su cumplimiento mediante la revisión del proceso periódico de depuración en tablas y esquemas. |
| Equipo de TI | Responsables de implementar las acciones y reglas de depuración de manera técnica. Ellos llevan a cabo la tarea de borrar o archivar las tablas o esquemas según las políticas de depuración. |
| DSI | Responsables de asegurar que la depuración y eliminación de datos se realice seguramente y que los datos confidenciales o sensibles se traten de acuerdo con sus políticas. |
| Analítica | Deberán de seguir las reglas de nomenclatura o de lo contrario sus tablan temporales serán depuradas. |

1. **Autorizadores**

| **Área** | **Puesto** | **Nombre** | **Autorización** |
| --- | --- | --- | --- |
| Gobierno de Datos | Director de Gobierno de Datos y Calidad | Víctor Mauricio Grzenda | Autorizado |
| Analítica Avanzada | Director de Analítica avanzada | Jonathan Ary Rubin  Leandro Guarnieri |  |
| Data Translator | Director Data Translator | Alejandro José Irigaray |  |
| Sistemas Big Data | Director de Sistemas Big Data | Arturo Burgos Balbuena |  |
___
# 📄 **[https://dillinger.io/Proceso Crystal - Data Translator 20240206.pptx](Proceso Crystal - Data Translator 20240206.pptx)** 
___

# Slide number: 1 -->

![Imagen 5](Imagen5.jpg)
Flujo de proceso para la creación de un Crystal
Data Translator

# Slide number: 2 -->
S5
 Proceso Crystal

![Imagen 6](Imagen6.jpg)

Análisis y entendimiento de la necesidad y expectativa del cliente

Obtención de reglas de negocio
S4
S3
S2
S1
Definición y modelado lógico de las entidades de datos

Validación del modelo propuesto con la unidad de negocio
Mapeo del modelo crystal vs insumos de capa curada/raw

Generación y validación de datos/resultados
Se adicionan en promedio 5 semanas de desarrollo en spark y productivización por parte de IT
Debe haber un entendimiento previo del flujo y relacionamiento de datos de las fuentes
Flujo para la creación de un crystal de complejidad baja (B), media (M) y alta (A) con tiempos estándar en semanas.
Documentación del requerimiento crystal para su envío a IT, incluyendo:

Insumos utilizados
Cálculo de variables, procedimientos de cruce y aplicación de reglas de negocio
Contenido y diccionarios de datos de las tablas crystal finales
Validación del crystal generado por IT-Dev en ambiente pre-productivo para asegurar que cumpla con las reglas/ características documentadas:

Definición/ejecución de validaciones

Dar visto bueno del desarrollo a IT
Relevamiento
Modelado lógico
Mapeo y validación del modelo
Validación
Documentación

![Imagen 72](Imagen72.jpg)

S7
S6
S4 – S5
S3
S1 – S2
S9
S7 – S8
S5 – S6
S3 – S4
S1 – S3
B
M
A

# Slide number: 3 -->
 Proceso Crystal
Los tiempos para la construcción de un Crystal podrían variar con base a la complejidad; dependiendo de la cantidad de outputs, cantidad de insumos y cálculos/reglas de
negocio, tomando en cuenta la capacidad del equipo.

![Imagen 4](Imagen4.jpg)
Asignación

![Imagen 7](Imagen7.jpg)
Complejidad

![Imagen 10](Imagen10.jpg)
Variará conforme la cantidad de proyectos a los que esté asignado una persona
___
# MarkItDown

[![PyPI](https://img.shields.io/pypi/v/markitdown.svg)](https://pypi.org/project/markitdown/)
![PyPI - Downloads](https://img.shields.io/pypi/dd/markitdown)
[![Built by AutoGen Team](https://img.shields.io/badge/Built%20by-AutoGen%20Team-blue)](https://github.com/microsoft/autogen)

> [!IMPORTANT]
> MarkItDown 0.0.2 alpha 1 (0.0.2a1) introduces a plugin-based architecture. As much as was possible, command-line and Python interfaces have remained the same as 0.0.1a3 to support backward compatibility. Please report any issues you encounter. Some interface changes may yet occur as we continue to refine MarkItDown to a first non-alpha release.

MarkItDown is a utility for converting various files to Markdown (e.g., for indexing, text analysis, etc).
It supports:
- PDF
- PowerPoint
- Word
- Excel
- Images (EXIF metadata and OCR)
- Audio (EXIF metadata and speech transcription)
- HTML
- Text-based formats (CSV, JSON, XML)
- ZIP files (iterates over contents)
- ... and more!

To install MarkItDown, use pip: `pip install markitdown`. Alternatively, you can install it from the source: 

```bash
git clone git@github.com:microsoft/markitdown.git
cd markitdown
pip install -e packages/markitdown
```

## Usage

### Command-Line

```bash
markitdown path-to-file.pdf > document.md
```

Or use `-o` to specify the output file:

```bash
markitdown path-to-file.pdf -o document.md
```

You can also pipe content:

```bash
cat path-to-file.pdf | markitdown
```

### Plugins

MarkItDown also supports 3rd-party plugins. Plugins are disabled by default. To list installed plugins:

```bash
markitdown --list-plugins
```

To enable plugins use:

```bash
markitdown --use-plugins path-to-file.pdf
```

To find available plugins, search GitHub for the hashtag `#markitdown-plugin`. To develop a plugin, see `packages/markitdown-sample-plugin`.

### Azure Document Intelligence

To use Microsoft Document Intelligence for conversion:

```bash
markitdown path-to-file.pdf -o document.md -d -e "<document_intelligence_endpoint>"
```

More information about how to set up an Azure Document Intelligence Resource can be found [here](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/how-to-guides/create-document-intelligence-resource?view=doc-intel-4.0.0)


### Python API

Basic usage in Python:

```python
from markitdown import MarkItDown

md = MarkItDown(enable_plugins=False) # Set to True to enable plugins
result = md.convert("test.xlsx")
print(result.text_content)
```

Document Intelligence conversion in Python:

```python
from markitdown import MarkItDown

md = MarkItDown(docintel_endpoint="<document_intelligence_endpoint>")
result = md.convert("test.pdf")
print(result.text_content)
```

To use Large Language Models for image descriptions, provide `llm_client` and `llm_model`:

```python
from markitdown import MarkItDown
from openai import OpenAI

client = OpenAI()
md = MarkItDown(llm_client=client, llm_model="gpt-4o")
result = md.convert("example.jpg")
print(result.text_content)
```

### Docker

```sh
docker build -t markitdown:latest .
docker run --rm -i markitdown:latest < ~/your-file.pdf > output.md
```
   
## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

### How to Contribute

You can help by looking at issues or helping review PRs. Any issue or PR is welcome, but we have also marked some as 'open for contribution' and 'open for reviewing' to help facilitate community contributions. These are ofcourse just suggestions and you are welcome to contribute in any way you like.


<div align="center">

|                       | All                                      | Especially Needs Help from Community                                                                 |
|-----------------------|------------------------------------------|------------------------------------------------------------------------------------------|
| **Issues**            | [All Issues](https://github.com/microsoft/markitdown/issues) | [Issues open for contribution](https://github.com/microsoft/markitdown/issues?q=is%3Aissue+is%3Aopen+label%3A%22open+for+contribution%22) |
| **PRs**               | [All PRs](https://github.com/microsoft/markitdown/pulls)     | [PRs open for reviewing](https://github.com/microsoft/markitdown/pulls?q=is%3Apr+is%3Aopen+label%3A%22open+for+reviewing%22)               |

</div>

### Running Tests and Checks

- Navigate to the MarkItDown package:

    ```sh
    cd packages/markitdown
    ```

- Install `hatch` in your environment and run tests:
    ```sh
    pip install hatch  # Other ways of installing hatch: https://hatch.pypa.io/dev/install/
    hatch shell
    hatch test
    ```

  (Alternative) Use the Devcontainer which has all the dependencies installed:
    ```sh
    # Reopen the project in Devcontainer and run:
    hatch test
    ```

- Run pre-commit checks before submitting a PR: `pre-commit run --all-files`

### Contributing 3rd-party Plugins

You can also contribute by creating and sharing 3rd party plugins. See `packages/markitdown-sample-plugin` for more details.


## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft
trademarks or logos is subject to and must follow
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
<!-- BEGIN MICROSOFT SECURITY.MD V0.0.9 BLOCK -->

## Security

Microsoft takes the security of our software products and services seriously, which includes all source code repositories managed through our GitHub organizations, which include [Microsoft](https://github.com/Microsoft), [Azure](https://github.com/Azure), [DotNet](https://github.com/dotnet), [AspNet](https://github.com/aspnet) and [Xamarin](https://github.com/xamarin).

If you believe you have found a security vulnerability in any Microsoft-owned repository that meets [Microsoft's definition of a security vulnerability](https://aka.ms/security.md/definition), please report it to us as described below.

## Reporting Security Issues

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report them to the Microsoft Security Response Center (MSRC) at [https://msrc.microsoft.com/create-report](https://aka.ms/security.md/msrc/create-report).

If you prefer to submit without logging in, send email to [secure@microsoft.com](mailto:secure@microsoft.com).  If possible, encrypt your message with our PGP key; please download it from the [Microsoft Security Response Center PGP Key page](https://aka.ms/security.md/msrc/pgp).

You should receive a response within 24 hours. If for some reason you do not, please follow up via email to ensure we received your original message. Additional information can be found at [microsoft.com/msrc](https://www.microsoft.com/msrc). 

Please include the requested information listed below (as much as you can provide) to help us better understand the nature and scope of the possible issue:

  * Type of issue (e.g. buffer overflow, SQL injection, cross-site scripting, etc.)
  * Full paths of source file(s) related to the manifestation of the issue
  * The location of the affected source code (tag/branch/commit or direct URL)
  * Any special configuration required to reproduce the issue
  * Step-by-step instructions to reproduce the issue
  * Proof-of-concept or exploit code (if possible)
  * Impact of the issue, including how an attacker might exploit the issue

This information will help us triage your report more quickly.

If you are reporting for a bug bounty, more complete reports can contribute to a higher bounty award. Please visit our [Microsoft Bug Bounty Program](https://aka.ms/security.md/msrc/bounty) page for more details about our active programs.

## Preferred Languages

We prefer all communications to be in English.

## Policy

Microsoft follows the principle of [Coordinated Vulnerability Disclosure](https://aka.ms/security.md/cvd).

<!-- END MICROSOFT SECURITY.MD BLOCK -->
# TODO: The maintainer of this repo has not yet edited this file

**REPO OWNER**: Do you want Customer Service & Support (CSS) support for this product/project?

- **No CSS support:** Fill out this template with information about how to file issues and get help.
- **Yes CSS support:** Fill out an intake form at [aka.ms/onboardsupport](https://aka.ms/onboardsupport). CSS will work with/help you to determine next steps.
- **Not sure?** Fill out an intake as though the answer were "Yes". CSS will help you decide.

*Then remove this first heading from this SUPPORT.MD file before publishing your repo.*

# Support

## How to file issues and get help  

This project uses GitHub Issues to track bugs and feature requests. Please search the existing 
issues before filing new issues to avoid duplicates.  For new issues, file your bug or 
feature request as a new Issue.

For help and questions about using this project, please **REPO MAINTAINER: INSERT INSTRUCTIONS HERE 
FOR HOW TO ENGAGE REPO OWNERS OR COMMUNITY FOR HELP. COULD BE A STACK OVERFLOW TAG OR OTHER
CHANNEL. WHERE WILL YOU HELP PEOPLE?**.

## Microsoft Support Policy  

Support for this **PROJECT or PRODUCT** is limited to the resources listed above.
## 01_Control_de_Versiones
| Unnamed: 0 | Cristal Data Control de Versiones | Unnamed: 2 | Unnamed: 3 | Unnamed: 4 |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |
|  | Versionamiento |  |  |  |
|  | No. de Versión | Fecha de cambio | Autor | Descripción |
|  | 1 | 2023-02-17 00:00:00 | Juan Carlos Cifuentes | Generación de Versión 1 del Documento |
|  | 1.1 | 20/07/2023 | Juan Carlos Cifuentes | Modificación de la estructura de la tabla de anonimato en zona curada |
|  | 1.01.01 | 22/08/2023 | Juan Carlos Cifuentes | Modificación del proceso para contemplar el filtro de Colores desde la Tabla RAW |
|  | 1.01.02 | 2023-12-09 00:00:00 | Juan Carlos Cifuentes | Adición de los campos banderadocumentodigital, y banderamercadotecnia a la tabla desde la zona curada, para validar los requerimientos legales |
|  | 1.01.03 | 15/9/2023 | Juan Carlos Cifuentes | Modificación del Catálogo de Tipo de Venta por temas de gobernanza |
|  | 1.01.04 | 25/9/2023 | Juan Carlos Cifuentes | Modificación de la Familia y Dominio, asi como eliminar el filtro de País en la consulta del paso 4 |
|  | 2.01.01 | 2023-11-17 00:00:00 | Juan Carlos Cifuentes | Generación del Crystal cd\_ekt\_pressupuestos\_anonimato, donde se disponibiliza la información de Red Unica, Tienda Física EKT, MasterID, CeCos, SKUs Comercios y SKUs SIE.<br>Se adicionan los filtros de Punto de Venta y filtrar los presupuestos con longitud 19 |
|  | 2.01.02 | 2023-11-21 00:00:00 | Juan Carlos Cifuentes | Modificación del paso 8 para indicar los campos relacionados a los productos de los presupuestos necesarios y el DER de la pestaña 5 |
|  | 2.01.03 | 2023-11-22 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>•\tPaso 1: Se cambia el comparador == por like ya que se debe quedar con los presupuestos que contenga las palabras COLOR, TEST o PRUEBA en el cliente<br>•\tPaso 4: Se excluye la información de Elektra.com (fisucursal != 9797) de los presupuestos<br>•\tPaso 5: Se excluye la información de Elektra.com (fisucursal != 9797) de los pedidos y cliente\_unico<br>•\tPaso 7: Aclaración de expandir la estructura detalle\_presupuesto a fila<br>•\tSe corrige el nombre de la variable descripcionTipoVenta en los pasos 5, 7,8,9,10 y 11<br> |
|  | 2.01.04 | 2023-01-10 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>•\tAdición de la lógica de constucción<br> |
|  | 2.01.5 | 2023-01-10 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>•\tAdición de la lógica de constucción<br> |
|  | 2.01.6 | 2023-01-23 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>•\tAdición de campos sensibles para el cruce de la información,<br> |
|  | 2.01.7 | 2023-02-08 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>• Apertura del Paso 15, con lo que se modifica desde el paso 11 hasta el 16<br>•Corrección del paso 22, moviendo los criterios de rekación a los filtros<br>Adicion del paso 25 para contemplar el mes anterior al último presupuesto<br> |
|  | 2.01.8 | 2023-02-12 00:00:00 | Juan Carlos Cifuentes | Modificación de:<br>A nivel presupuesto contemplar dos estatus adicionales a CeCos y dos campos solicitados por el usuario<br>• Eliminación de paso 1 y 2 en persona-envio<br>•Mover el paso 25 al 3<br>•Contemplar la modificación de la estandarización express generando un paso 10 con indicadores consolidados<br>•Uso de la tabla paso 10 para cruzar con datos\_contacto\_master<br>•Modificación de las marcas para construirse con base al masterID<br> |
|  | 2.01.09 | 29/2/2023 | Juan Carlos Cifuentes | Modificación de:<br>Modificación del Paso 4,6,7,8,9 y 10 para incluir la calificación del correo y celular para el cruce eidentificación del MasterID<br>Modificación del paso 8 quitando eldescencriptar de la tabla B (Frecuencia)<br>Adición de criterio en curado dado la última regla del correo para la estandarización<br> |
|  | 2.01.10 | 2023-02-14 00:00:00 | Juan Carlos Cifuentes | Modificación de los nombres para alinear a marco de nomenclatura del lake<br> |
|  | 2.02.01 | 2023-02-17 00:00:00 | Juan Carlos Cifuentes | Requerimiento de IT se documentaran por separado las entidades, contemplando en este documento la entidad persona<br> |
|  | 2.02.02 | 2024-07-29 00:00:00 | Oswaldo Chávez Mogollán | Actualización de cliente unico, masterid, e indicadores: EsPedido, EsPptoCredito, EsCredito, ClienteUnico<br> |
|  | 2.02.03 | 2024-09-02 00:00:00 | Oswaldo Chávez Mogollán | Actualización de espersonaconocida<br> |

## 02_CD_Presentación_Producto
| Unnamed: 0 | Cristal Data Presentación del Producto | Unnamed: 2 |
| --- | --- | --- |
|  |  |  |
|  | Información general del Cristal Data |  |
|  | Nombre(s) tabla(s) Final(es): | cd\_ekt\_prospecto\_cte\_canales\_envio |
|  | Descripción: | Cristal Data que permitirá sacar del anonimato a los clientes que envían información del presupuesto. Para esto se disponibiliza dos tablas para responder las preguntas:<br>- Presupuestos: ¿qué presupuestos se han enviando a los Clientes/Prospectos ?¿Que productos se presupuestan por tienda y región?¿qué presupuestos se convirtieron en un pedido?<br><br>Este Crystal dara respuesta a la presentación de DG y también se podrá identificar que presupuestan los clientes para entender y mejorar la experiencia del cliente, permitiendo tener datos para proponer campañas o comunicados entendiendo que presupuestan y si es a crédito o contado |
|  | Familia: | Cliente y presupuesto |
|  | Empresa: | Elektra |
|  | Dominio: | Personas |
|  | Periodicidad de la ejecución (diaria,semanal, mensual, et.): | Diaria |
|  | Tipo de Actualización (full, delta, etc. | Delta |
|  | Profundidad Histórica: | Requiere desde junio de 2023 en adlentare |
|  | Nivel de Granularidad | Presupuesto y SKU de tienda física EKT |
|  | Grupos de Usuarios | Karen Altagracia Olivo Santana y Alfa Berenice |

## 03_CD_Insumos
| Unnamed: 0 | Cristal Data Insumos | Unnamed: 2 | Unnamed: 3 | Unnamed: 4 | Unnamed: 5 | Unnamed: 6 | Unnamed: 7 | Unnamed: 8 | Unnamed: 9 | Unnamed: 10 | Unnamed: 11 | Unnamed: 12 | Unnamed: 13 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  | Detalles de los Insumos de los cuales depende |  |  |  |  |  |  |  |  |  |  |  |  |
|  | No. | Plataforma | Objeto | Esquema | Tabla | Campo | PK (1=pk, 2=fk, 0= Otro) |  |  |  |  |  |  |
|  | 1 | Cloudera kio |  | cd\_ekt\_bdclientes | cd\_ekt\_prospecto\_cte\_presupuesto | TiendaID | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | PresupuestoID | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | SkuId | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | esPedido | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteUnico | 0 |  |  |  |  |  |  |
|  | 2 | Cloudera kio |  | cu\_bdekt | cu\_ekt\_clientes\_prospecto | PaisID | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | NombreDocumento | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | TicketID | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteCorreo | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | DocumentoID | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | NumeroEconomicoSucursal | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | tipocanalid | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | nombretipocanal | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | banderadocumentodigital | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | banderamercadotecnia | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | fecharegistro | 1 |  |  |  |  |  |  |
|  | 3 | Cloudera kio |  | cu\_bdekt | cu\_deyde\_vwdatainfo\_clienteanonimo\_nombre | IDE | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | IdentificadorDocumento | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | FcNumeroEconomico | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | FCTipoCanalID | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteNombre | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteNombreNexo | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteApellidoPaterno | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteApellidoNexos | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ClienteApellidoMaterno | 0 |  |  |  |  |  |  |
|  | 4 | Cloudera kio |  | cu\_bdekt | cu\_deyde\_vwdatainfo\_clienteanonimo\_correo | IDE | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | IdentificadorDocumento | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | FcNumeroEconomico | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | FCTipoCanalID | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | dir\_ema | 0 |  |  |  |  |  |  |
|  | 5 | Cloudera kio |  | cu\_bdekt | cu\_deyde\_vwdatainfo\_clienteanonimo\_telefono | IDE | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | IdentificadorDocumento | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | FcNumeroEconomico | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | FCTipoCanalID | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | numtel1 | 0 |  |  |  |  |  |  |
|  | 6 | Cloudera kio |  | cu\_baz\_bdclientes | cu\_ta\_frecuencia\_email | dir\_email | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | frecuencia | 0 |  |  |  |  |  |  |
|  | 7 | Cloudera kio |  | cu\_baz\_bdclientes | cu\_baz\_bdclientes.cu\_ta\_frecuencia\_tel1 | indtip1 | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | tel1\_norm | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | frecuencia | 0 |  |  |  |  |  |  |
|  | 8 | Cloudera kio |  | cd\_baz\_bdclientes | cd\_cte\_datos\_contacto\_master | id\_master | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | nexos\_apellido\_paterno | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | apellido\_paterno\_norm | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | nexos\_apellido\_materno | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | apellido\_materno\_norm | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | nombre\_norm | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | tel1\_norm | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | tel2\_norm | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | dir\_email | 0 |  |  |  |  |  |  |
|  | 9 | Cloudera KIO |  | cd\_baz\_bdclientes | cd\_cte\_master | id\_master | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | id\_cliente | 2 |  |  |  |  |  |  |
|  | 10 | Cloudera KIO |  | rd\_baz\_bdclientes | rd\_MCDT403 | t403\_num\_clte | 1 |  |  |  |  |  |  |
|  | 11 | Cloudera KIO |  | cd\_ baz\_bdclientes | cd\_cap\_cuenta\_sem | id\_master | 1 |  | B |  | B |  | B |
|  |  |  |  |  |  | cod estatus | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | cod\_titular | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | cod\_producto | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | cod\_subprod | 0 |  |  |  |  |  |  |
|  | 12 | Cloudera KIO |  | cu\_gs\_bosopoperlog | cu\_ebx\_catm\_gs\_productos\_captacion\_niveles | fcnuevo\_producto\_nivel\_03 | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fcnuevo\_producto\_nivel\_04 | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fcnuevo\_producto\_nivel\_05 | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fccodigo\_subproducto | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | fccodigo\_producto | 1 |  |  |  |  |  |  |
|  | 13 | Cloudera kio |  | cu\_gs\_bdsopoperlog | cu\_ebx\_catm\_gs\_fitires\_niveles | fccredimax\_fitir | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | fcnivel\_1 | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fcnivel\_2 | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fcnivel\_3 | 0 |  |  |  |  |  |  |
|  | 14 | Cloudera KIO |  | cd\_baz\_bdclientes | cd\_cre\_detalle\_pedido | id\_master | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | id\_cliente | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | est\_pedido | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | ind\_credventagestora | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | ind\_reasignacion | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fec\_liquidacion | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fec\_cancelacion | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | cod\_fiti | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | fccredimax\_fitir | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | id\_pedido\_pais | 0 |  |  |  |  |  |  |
|  | 15 | Cloudera KIO |  | cd\_baz\_bdclientes | cd\_cte\_empleado\_master | id\_master | 1 |  |  |  |  |  |  |
|  | 16 | Cloudera KIO |  | cd\_baz\_bdclientes | cd\_con\_cte\_actividad\_mes | id\_master | 1 |  |  |  |  |  |  |
|  |  |  |  |  |  | ind\_activo | 0 |  |  |  |  |  |  |
|  |  |  |  |  |  | Num\_Periodo\_mes | 0 |  |  |  |  |  |  |

## 04_CD_Relacion_TBLS_RAW
| Unnamed: 0 | Crystal Data Relación de Tablas RAW | Unnamed: 2 | Unnamed: 3 |
| --- | --- | --- | --- |
|  |  |  |  |
|  | Relación de Tablas RAW es decir Insumos que se requieren para la construcción cd\_ekt\_persona\_envio |  |  |
|  | Paso 1 |  |  |
|  | Descripción | Cruce con información del pedido |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cd\_ekt\_prospecto\_cte\_presupuesto |  |
|  | Tabla B: |  |  |
|  | Relación: |  |  |
|  | Tipo de Unión: |  |  |
|  | Columnas Finales | tiendaID, presupuestoID<br>, max(esPedido) esPedido, <br>, max(B.ClienteUnico) ClienteUnicoPedido,<br>, if(max(TipoVentaID = 2),1,0) as EsPptoCredito |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio | Agrupar por los campos tiendaID, presupuestoID |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_anonimato\_persona\_ppto |  |
|  |  |  |  |
|  | Paso 2 |  |  |
|  | Descripción | Tabla temporal con los Tickets Presupuestos de red única y datos de personas |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cu\_bdekt.cu\_ekt\_cte\_prospecto |  |
|  | Relación: |  |  |
|  | Tipo de Unión: |  |  |
|  | Columnas Finales | cast (ROW\_NUMBER() over (order by numeroeconomicosucursal, documentoid, tipocanalid) as string) as id <br>, numeroeconomicosucursal, documentoid, tipocanalid<br>, nombretipocanal , banderadocumentodigital, banderamercadotecnia, fecharegistro |  |
|  | Filtro y/o condiciones | TipoTicketID = 1 <br>PaisId = 1 <br>NombreDocumento = "Presupuesto"<br>cast(NumeroEconomicoSucursal as int) > 99<br>DocumentoID not in ("0","") and length(DocumentoID) !=19(<br>( clientecorreo not like '%"%' | clientecorreo is null) |  |
|  | Reglas negocio | No se filtra por fecha ya que la estandarización express solo contempla los filtros indicados en este paso |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_anonimato\_persona |  |
|  |  |  |  |
|  | Paso 3 |  |  |
|  | Descripción | Tabla temporal con los Tickets Presupuestos de red única |  |
|  | Origen Tablas Temporales | Paso 1 y Paso 2 |  |
|  | Tabla A: | TEMP\_anonimato\_persona\_ppto |  |
|  | Tabla B: | TEMP\_anonimato\_persona |  |
|  | Relación: | A.tiendaID = B.numeroeconomicosucursal<br>A.presupuestoID = B.documentoid |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | Distinct A.tiendaID, A.presupuestoID, A.esPedido, A.ClienteUnicoPedido, A.EsPptoCredito<br>B.id, B.tipocanalid, B.nombretipocanal , B.banderadocumentodigital, B.banderamercadotecnia, B.fecharegistro |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_base\_persona |  |
|  |  |  |  |
|  |  |  |  |
|  | Paso 4 |  |  |
|  | Descripción | Tabla Temporal aplicando criterios de calidad de laestandarización expres |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cu\_bdekt.cu\_deyde\_vwdatainfo\_clienteanonimo\_nombre |  |
|  | Tabla B: | cu\_bdekt.cu\_deyde\_vwdatainfo\_clienteanonimo\_correo |  |
|  | Relación: | A.ide=B.ide and B.fitipocanalenvid=2 |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid<br> , if( (dir\_ema='3' and fs\_ema='9') or (dir\_ema='2' and fs\_ema='7'),1,0) marcaCorreo<br> , concat\_ws(' ',descencriptar(A.nombre), A.nexos1, descencriptar(A.apell1), A.nexos2 ,descencriptar(A.apell2)) AS nombrecompleto\_norm, ,A.nombre, A.nexos1, A.apell1, A.nexos2, A.apell2<br> , dd\_ema, fd\_ema, fs\_ema, dir\_ema<br> , descencriptar(dd\_ema) dir\_email<br> , if( fd\_ema.isin('B','F') ,0, Cast( fd\_ema as int)) as indema<br> , if( fs\_ema = 'B' and fd\_ema = 'B',0,1) as EMA\_COMP\_NULO<br> , if( fs\_ema = 'F' and fd\_ema = 'F',0,1) as EMA\_COMP\_FICT<br> , if( fs\_ema in ('0', '2') and fd\_ema in ('0', '3', '7', '6'), 0, 1) as EMA\_CONF\_SINT <br> , if( fs\_ema = '0' and fd\_ema in ('0', '3', '7', '6'), 0, 1) as EMA\_PREC\_DOMI <br> , if( fs\_ema = '0' and fd\_ema in ('3', '7'), 0, 1) as EMA\_REME\_SINT<br> , if( fs\_ema = '0' and fd\_ema in ('6', '8'), 0, 1) as EMA\_REME\_DOMI<br> , if( substr( dd\_ema,instr( descencriptar(dd\_ema) ,'@')+ 1) in ('gmail.com', 'hotmail.com', 'outlook.com','yahoo.com.mx', 'live.com.mx', 'yahoo.com', 'live.com', 'hotmail.es', 'prodigy.net.mx', 'msn.com', 'outlook.es', 'icloud.com', 'yahoo.es','onewaymail.com', 'latinmail.com', 'terrD.com.mx', 'aol.com', 'facebook.com', 'rocketmail.com', 'itelcel.com', 'bbvD.com', 'pemex.com','live.com.ar', 'comunidad.unam.mx', 'imss.gob.mx', 'cfe.gob.mx', 'telmexmail.com', 'inegi.org.mx', 'hotmail.com.ar', 'banorte.com','yahoo.fr', 'ciencias.unam.mx', 'cablevision.net.mx', 'uabc.edu.mx', 'ipn.mx'), 1, 0) as EMA\_PREC\_CATA |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_NFR\_CORREO |  |
|  |  |  |  |
|  | Paso 5 |  |  |
|  | Descripción | Cruce temporal con la frecuencia del número del correo |  |
|  | Origen Tablas Temporales | Paso 4 |  |
|  | Tabla A: | TEMP\_NFR\_CORREO |  |
|  | Tabla B: | cu\_baz\_bdclientes.cu\_ta\_frecuencia\_email |  |
|  | Relación: | A.dir\_email = B.dir\_email |  |
|  | Tipo de Unión: | Left join |  |
|  | Columnas Finales | ide, fcnumeroeconomico, identificadordocumento, fitipocanalenvid<br> , dd\_ema, fs\_ema, dir\_ema<br> , marca\_correo, nombrecompleto\_norm, nombre, nexos1, apell1, nexos2, apell2<br> , 1 as id\_delta<br> , CASE WHEN A.dd\_ema IS NULL or A.dd\_ema = '' THEN 0 WHEN B.frecuencia >= 10 THEN 0 ELSE 1 END EMA\_DUPL\_REPT<br> , CASE WHEN A.fd\_ema in ( 'B' , 'F') THEN 0 ELSE CAST(A.fd\_ema AS INT) END indema<br> , A.EMA\_COMP\_NULO<br> , A.EMA\_COMP\_FICT<br> , A.EMA\_CONF\_SINT<br> , A.EMA\_PREC\_DOMI<br> , A.EMA\_REME\_SINT<br> , A.EMA\_REME\_DOMI<br> , A.EMA\_PREC\_CATA<br>  , dir\_email<br> |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_FREUENCIA\_CORREO |  |
|  |  |  |  |
|  | Paso 6 |  |  |
|  | Descripción | Generación de tabla temporal con los correos y su calificación de la estandarización |  |
|  | Origen Tablas Temporales | Paso 5 |  |
|  | Tabla A: | TEMP\_FREUENCIA\_CORREO |  |
|  | Relación: |  |  |
|  | Tipo de Unión: |  |  |
|  | Columnas Finales | IDE, fcnumeroeconomico, identificadordocumento, fitipocanalenvid, dir\_email, dd\_ema<br> , Round(((indema \* 0.05 + greatest(0,1 - (1 - EMA\_COMP\_NULO) - (1 - EMA\_COMP\_FICT) - 0.5 \* (1 - EMA\_CONF\_SINT) - 0.5 \* (1 - EMA\_PREC\_DOMI) - 0.1 \* (1 - EMA\_REME\_SINT) - 0.1 \* (1 - EMA\_REME\_DOMI) - 0.75 \* (1 - EMA\_DUPL\_REPT) - 0.4 \* (1- EMA\_PREC\_CATA)) \* 0.5)),4) as ICN\_EMAIL<br>, case when Round(((indema \* 0.05 + greatest(0,1 - (1 - EMA\_COMP\_NULO) - (1 - EMA\_COMP\_FICT) - 0.5 \* (1 - EMA\_CONF\_SINT) - 0.5 \* (1 - EMA\_PREC\_DOMI) - 0.1 \* (1 - EMA\_REME\_SINT) - 0.1 \* (1 - EMA\_REME\_DOMI) - 0.75 \* (1 - EMA\_DUPL\_REPT) - 0.4 \* (1- EMA\_PREC\_CATA)) \* 0.5)),4) < 0.50 then '5.Nulo' when Round(((indema \* 0.05 + greatest(0,1 - (1 - EMA\_COMP\_NULO) - (1 - EMA\_COMP\_FICT) - 0.5 \* (1 - EMA\_CONF\_SINT) - 0.5 \* (1 - EMA\_PREC\_DOMI) - 0.1 \* (1 - EMA\_REME\_SINT) - 0.1 \* (1 - EMA\_REME\_DOMI) - 0.75 \* (1 - EMA\_DUPL\_REPT) - 0.4 \* (1- EMA\_PREC\_CATA)) \* 0.5)),4) < 0.70 then '4.Malo' twhen Round(((indema \* 0.05 + greatest(0,1 - (1 - EMA\_COMP\_NULO) - (1 - EMA\_COMP\_FICT) - 0.5 \* (1 - EMA\_CONF\_SINT) - 0.5 \* (1 - EMA\_PREC\_DOMI) - 0.1 \* (1 - EMA\_REME\_SINT) - 0.1 \* (1 - EMA\_REME\_DOMI) - 0.75 \* (1 - EMA\_DUPL\_REPT) - 0.4 \* (1- EMA\_PREC\_CATA)) \* 0.5)),4) < 0.85 then '3.Regular' else '2.Bueno' end as ICC\_EMAIL<br>, IF( (ICC\_EMAIL == '3.Regular') and marca\_correo = 1 and trim(nombrecompleto\_norm) not in (' ','') and trim(dir\_email)!="" , 1, 0) FlagCorreo<br>, nombre, nexos1, apell1, nexos2, apell2, nombrecompleto\_norm |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_CORREO |  |
|  |  |  |  |
|  | Paso 7 |  |  |
|  | Descripción | Tabla Temporal aplicando criterios de calidad de la estandarización express para número de teléfono |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cu\_bdekt.cu\_deyde\_vwdatainfo\_clienteanonimo\_nombre |  |
|  | Tabla B: | cu\_bdekt.cu\_deyde\_vwdatainfo\_clienteanonimo\_telefono |  |
|  | Relación: | A.ide=B.ide and and B.fitipocanalenvid!=2 |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid<br>IF(B.indtel1 IS NULL AND B.indver1 IS NULL,0, IF(B.indtel1 = '0' AND B.indver1 IN('0','1'),0,1)) AS CEL\_COMP\_NULO , <br> IF(descencriptar(numtel1) ='' OR descencriptar(numtel1) IS NULL,0, IF (LENGTH(B.numtel1) = 10,1,0)) AS CEL\_CONF\_LONG , <br> IF(B.indtel1 IS NULL AND B.indver1 IS NULL,0, IF (B.indtel1 = '5' AND B.indver1 = '6',0,1)) AS CEL\_PREC\_NOTE , <br> IF(B.indtel1 IS NULL AND B.indver1 IS NULL,0, IF (B.indtel1 = '2' AND B.indver1 IN ('2','3','4','5'),0,1)) AS CEL\_REME\_LAAC , <br> IF(descencriptar(B.numtel1) IS NULL OR descencriptar(B.numtel1) = '',0, IF( descencriptar(B.numtel1) LIKE'%01234%' OR descencriptar(B.numtel1) LIKE'%12345%' OR descencriptar(B.numtel1) LIKE'%23456%' OR descencriptar(B.numtel1) LIKE'%34567%' OR descencriptar(B.numtel1) LIKE '%45678%' OR descencriptar(B.numtel1) LIKE'%56789%',0,1)) AS CEL\_VALI\_SECU , <br> IF(descencriptar(B.numtel1) IS NULL OR A.descencriptar(B.numtel1) ='',0, IF.descencriptar(B.numtel1) LIKE'%00000%',0,1)) AS CEL\_VALI\_CERO , <br> IF(descencriptar(B.numtel1) IS NULL OR descencriptar(B.numtel1) ='',0, IF(descencriptar(B.numtel1) = REGEXP\_REPLACE(descencriptar(B.numtel1) ,'[^0-9]','0'),1,0)) AS CEL\_CONF\_NUME , <br> B.numtel1 , B.indtip1 , B.indtel1 ,B.indvar1<br>, descencriptar(B.numtel1) celular1<br>, concat\_ws(' ',descencriptar(A.nombre), A.nexos1, descencriptar(A.apell1), nexos2 ,descencriptar(A.apell2)) AS nombrecompleto\_norm, A.nombre, A.nexos1, A.apell1, A.nexos2, A.apell2<br>IF( ( (indtel1='2' and indver1='2') OR (indtel1='2' and indver1='3') OR (indtel1='4' and indver1='7')),1,0) MarcaCelular<br> |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_NFR\_CELULAR |  |
|  |  |  |  |
|  | Paso 8 |  |  |
|  | Descripción | Cruce temporal con la frecuencia del número del celular |  |
|  | Origen Tablas Temporales | Paso 7 |  |
|  | Tabla A: | TEMP\_NFR\_CELULAR |  |
|  | Tabla B: | cu\_baz\_bdclientes.cu\_ta\_frecuencia\_tel1 |  |
|  | Relación: | A.numtel1 = B.tel1\_norm AND A.indtip1 = B.indtip1 |  |
|  | Tipo de Unión: | Left join |  |
|  | Columnas Finales | A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid<br>, 1 AS id\_delta <br> ,CASE WHEN celular1 or celular1= '' THEN 0 WHEN B.frecuencia IS NOT NULL THEN CASE WHEN A.indtip1 = 'M' then IF(B.frecuencia >=4,0,1) WHEN A.indtip1 = 'F' then IF(B.frecuencia >=7,0,1) ELSE 1 END ELSE 1 END CEL\_DUPL\_REPT <br> , CEL\_COMP\_NULO <br> , CEL\_CONF\_LONG <br> , CEL\_CONF\_NUME <br> , CEL\_REME\_LAAC <br> , CEL\_PREC\_NOTE <br> , CEL\_VALI\_SECU <br> , CEL\_VALI\_CERO <br> ,A.numtel1 <br> ,A.indtip1 <br> ,A.ndtel1 ,indvar1, celular1<br>, MarcaCelular , nombre, nexos1, apell1, nexos2, apell2, nombrecompleto\_norm<br> |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_FREUENCIA\_CELULAR |  |
|  |  |  |  |
|  | Paso 9 |  |  |
|  | Descripción | Generación de tabla temporal con los correos y su calificación de la estandarización |  |
|  | Origen Tablas Temporales | Paso 8 |  |
|  | Tabla A: | TEMP\_FREUENCIA\_CELULAR |  |
|  | Relación: |  |  |
|  | Tipo de Unión: |  |  |
|  | Columnas Finales | A.numtel1 ,A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid , celular1, <br>, Round(((cASt(A.indtel1 AS INT) \* 0.05 + GREATEST(0,1 - (1 - A.CEL\_COMP\_NULO) - 0.5 \* (1 - A.CEL\_CONF\_LONG) - 0.5 \* (1 - A.CEL\_CONF\_NUME) - 0.75 \* (1 - A.CEL\_DUPL\_REPT)- 0.25 \* (1 - A.CEL\_REME\_LAAC) - 0.10 \*(1 - A.CEL\_PREC\_NOTE) - 0.5 \* (1 - A.CEL\_VALI\_SECU) - 0.5 \* (1 - A.CEL\_VALI\_CERO)) \* 0.5)),4) AS ICN\_CELULAR <br>,CASE WHEN ROUND(((cASt(A.indtel1 AS INT) \* 0.05 + GREATEST(0,1 - (1 - A.CEL\_COMP\_NULO) - 0.5 \* (1 - A.CEL\_CONF\_LONG) - 0.5 \* (1 - A.CEL\_CONF\_NUME) - 0.75 \* (1 - A.CEL\_DUPL\_REPT)- 0.25 \* (1 - A.CEL\_REME\_LAAC) - 0.10 \* (1 - A.CEL\_PREC\_NOTE) - 0.5 \* (1 - A.CEL\_VALI\_SECU) - 0.5 \* (1 - A.CEL\_VALI\_CERO)) \* 0.5)),4) < 0.5 THEN '5.Nulo' <br>WHEN ROUND(((cASt(A.indtel1 AS INT) \* 0.05 + GREATEST(0,1 - (1 - A.CEL\_COMP\_NULO) - 0.5 \* (1 - A.CEL\_CONF\_LONG) - 0.5 \* (1 - A.CEL\_CONF\_NUME) - 0.75 \* (1 - A.CEL\_DUPL\_REPT)- 0.25 \* (1 - A.CEL\_REME\_LAAC) - 0.10 \* (1 - A.CEL\_PREC\_NOTE) - 0.5 \* (1 - A.CEL\_VALI\_SECU) - 0.5 \* (1 - A.CEL\_VALI\_CERO)) \* 0.5)),4) < 0.70 THEN '4.Malo' <br>WHEN ROUND(((cASt(A.indtel1 AS INT) \* 0.05 + GREATEST(0,1 - (1 - A.CEL\_COMP\_NULO) - 0.5 \* (1 - A.CEL\_CONF\_LONG) - 0.5 \* (1 - A.CEL\_CONF\_NUME) - 0.75 \* (1 - A.CEL\_DUPL\_REPT)- 0.25 \* (1 - A.CEL\_REME\_LAAC) - 0.10 \* (1 - A.CEL\_PREC\_NOTE) - 0.5 \* (1 - A.CEL\_VALI\_SECU) - 0.5 \* (1 - A.CEL\_VALI\_CERO)) \* 0.5)),4) < 0.85 THEN '3.Regular' <br>ELSE '2.Bueno' END AS ICC\_CELULAR <br>, IF( ( ICC\_CELULAR == '3.Regular') and (MarcaCelular = 1) and trim(nombrecompleto\_norm) not in (' ','') and trim(celular1)!="", 1, 0) FlagCelular<br>, nombre, nexos1, apell1, nexos2, apell2, nombrecompleto\_norm |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_CELULAR |  |
|  |  |  |  |
|  | Paso 10 |  |  |
|  | Descripción | Tabla temporal para la frecuencia del correo |  |
|  | Origen Tablas Temporales | Paso 9 y Paso 6 |  |
|  | Tabla A: | TEMP\_CORREO |  |
|  | Tabla B: | TEMP\_CELULAR |  |
|  | Relación: | A.ide=B.ide <br>and A.fcnumeroeconomico= B.fcnumeroeconomico and A.identificadordocumento = B.identificadordocumento and A.fitipocanalenvid = B.fitipocanalenvid |  |
|  | Tipo de Unión: | UNION |  |
|  | Columnas Finales | ( A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid <br>, A.nombre ClienteNombre, A.nexos1 ClienteNombreNexo, A.apell1 ClienteApellidoPaterno, A.nexos2 ClienteApellidoNexos, A.apell2 ClienteApellidoMaterno<br>, A.nombrecompleto\_norm<br>, A.dd\_ema ClienteCorreo, A.ICN\_EMAIL ClienteIndicadorCorreo, A.ICC\_EMAIL ClienteCalificaciónCorreo, A.FlagCorreo, A.dir\_email<br>, "N/A" as ClienteCelular, -1.0 ClienteIndicadorCelular, "5.Nulo" ClienteCalifcacionCelular, 0 FlagCelular, "N/A" celular1)<br>union all <br>( B.ide, B.fcnumeroeconomico, B.identificadordocumento, B.fitipocanalenvid <br>, B.nombre ClienteNombre, B.nexos1 ClienteNombreNexo, B.apell1 ClienteApellidoPaterno, B.nexos2 ClienteApellidoNexos, B.apell2 ClienteApellidoMaterno, B.nombrecompleto\_norm<br>, "N/A" as ClienteCorreo, -1.0 ClienteIndicadorCorreo, "5.Nulo" as ClienteCalificacionCorreo, 0 FlagCorreo, "N/A" as dir\_email<br>, B.numtel1 ClienteCelular, B.ICN\_CELULAR ClienteIndicadorCelular, B.ICC\_CELULAR ClienteCalifcaciónCelular, B.FlagCelular, B.celular1) |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_BASE\_EXT |  |
|  |  |  |  |
|  | Paso 11 |  |  |
|  | Descripción | Tabla temporal para la generación de MasterID para cruzar de acuerdo al cliente único |  |
|  | Origen Tablas Temporales | Paso 10 |  |
|  | Tabla A: | TEMP\_BASE\_EXT |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_cte\_datos\_contacto\_master |  |
|  | Relación: | A.dir\_email = B.dir\_email <br> trim(A.nombrecompleto\_norm),<br> trim( concat\_ws(' ',B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm) ) <br> ) >= 90 ) <br>trim(concat\_ws(' ', B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm)) not in (' ','') |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid , B.id\_master |  |
|  | Filtro y/o condiciones | FlagCorreo = 1 |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_NOMBRE\_CORREO |  |
|  |  |  |  |
|  | Paso 12 |  |  |
|  | Descripción | Tabla temporal para la generación de MasterID para cruzar de acuerdo al cliente único |  |
|  | Origen Tablas Temporales | Paso 10 |  |
|  | Tabla A: | TEMP\_BASE\_EXT |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_cte\_datos\_contacto\_master |  |
|  | Relación: | (B.tel1\_norm = A.celular1) & (B.tel1\_norm!='5555555555')<br>(100 - LEVENSHTEIN(<br> trim(A.nombrecompleto\_norm),<br> trim( concat\_ws(' ',B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm) ) <br> ) >= 90 )<br>trim(concat\_ws(' ', B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm)) not in (' ','') |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid , B.id\_master |  |
|  | Filtro y/o condiciones | FlagCelular = 1 |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_NOMBRE\_TELEFONO1 |  |
|  |  |  |  |
|  | Paso 13 |  |  |
|  | Descripción | Tabla temporal para la generación de MasterID para cruzar de acuerdo al cliente único |  |
|  | Origen Tablas Temporales | Paso 10 |  |
|  | Tabla A: | TEMP\_BASE\_EXT |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_cte\_datos\_contacto\_master |  |
|  | Relación: | (B.tel2\_norm = A.celular1) & (B.tel2\_norm !='5555555555')<br>(100 - LEVENSHTEIN(<br> trim(A.nombrecompleto\_norm),<br> trim( concat\_ws(' ',B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm) ) <br> ) >= 90 )<br>trim(concat\_ws(' ', B.nombre\_norm, B.nexos\_apellido\_paterno, B.apellido\_paterno\_norm, B.nexos\_apellido\_materno, B.apellido\_materno\_norm)) not in (' ','') |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid , B.id\_master |  |
|  | Filtro y/o condiciones | FlagCelular = 1 |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_NOMBRE\_TELEFONO2 |  |
|  |  |  |  |
|  | Paso 14 |  |  |
|  | Descripción | Relación temporal con el ID\_Master por coincidencia de teléfono ocorreo |  |
|  | Origen Tablas Temporales | Paso 11, Paso 12 Y Paso 13 |  |
|  | Tabla A: | TEMP\_RELACION\_NOMBRE\_CORREO |  |
|  | Tabla B: | TEMP\_RELACION\_NOMBRE\_TELEFONO1 |  |
|  | Tabla B: | TEMP\_RELACION\_NOMBRE\_TELEFONO2 |  |
|  | Relación: |  |  |
|  | Tipo de Unión: | UNION |  |
|  | Columnas Finales | select \* from relacion\_nombre\_telefono1<br> union<br> select \* from relacion\_nombre\_telefono2<br> union<br> select \* from relacion\_nombre\_correo |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  |  |  |  |
|  | Paso 15 |  |  |
|  | Descripción | Tabla temporal para la generación de MasterID para cruzar de acuerdo al cliente único |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cd\_baz\_bdclientes.cd\_cte\_master |  |
|  | Relación: |  |  |
|  | Tipo de Unión: |  |  |
|  | Columnas Finales | min(id\_master) as id\_master,<br> id\_cliente as ClienteUnico |  |
|  | Filtro y/o condiciones | Obtener el minimo del ID\_Master<br>cod\_tipo\_cliente='CLIENTE\_UNICO' |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_MasterID\_1 |  |
|  |  |  |  |
|  | Paso 16 |  |  |
|  | Descripción | Generación de tabla temporal con el cliente unico |  |
|  | Origen Tablas Temporales | Paso 14 y Paso 15 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla B: | TEMP\_MasterID\_1 |  |
|  | Relación: | A. id\_master = B. id\_master |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | distinct A.id\_master, B.ClienteUnico |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_CU |  |
|  |  |  |  |
|  | Paso 17 |  |  |
|  | Descripción | Identificación si es digital |  |
|  | Origen Tablas Temporales | Paso 16 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID\_CU |  |
|  | Tabla B: | rd\_baz\_bdclientes.rd\_MCDT403 |  |
|  | Relación: | A.ClienteUnico = B.t403\_num\_clte |  |
|  | Tipo de Unión: | left join |  |
|  | Columnas Finales | A.id\_master, <br>collect\_set(ClienteUnico) ClienteUnico<br>max(case when A.id\_master is not null and A.ClienteUnico is not null then 1 else 0 end) marcaProceso<br>max(case when B.t403\_num\_clte is not null then 1 else 0 end) esDigital |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_DIGITAL |  |
|  |  |  |  |
|  | Paso 18 |  |  |
|  | Descripción | Adición del Crystal de Crédito |  |
|  | Origen Tablas Temporales | Paso 14 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla B: | cd\_ baz\_bdclientes.cd\_cap\_cuenta\_sem |  |
|  | Tabla C: | cu\_gs\_bosopoperlog.cu\_ebx\_catm\_gs\_productos\_captacion\_niveles |  |
|  | Relación: | A.id\_master = B.id\_master<br>B.cod\_producto = C.fccodigo\_producto AND B.cod\_subprod = C. fccodigo\_subproducto<br>AND B.COD\_TITULAR = 'T' and B.cod estatus = "'ACTIVA"<br>AND UPPER (C.fcnuevo\_producto\_nivel\_03) like "%CAPTACION%"<br>AND (UPPER(C.fcnuevo\_producto\_nivel\_04) like "%INVERSION%" OR UPPER(C.fcnuevo\_producto\_nivel\_05) like "%DEBIT0%" OR UPPER(C.fcnuevo\_producto\_nivel\_05) like "%GUARDADIT0%") |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT Aid\_master |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_CAPTA |  |
|  |  |  |  |
|  | Paso 19 |  |  |
|  | Descripción | Adición del Crystal de Crédito |  |
|  | Origen Tablas Temporales | Paso 14 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_cre\_detalle\_pedido |  |
|  | Tabla C: | cu\_gs\_bdsopoperlog.cu\_ebx\_catm\_gs\_fitires\_niveles |  |
|  | Relación: | A.id\_master = B.id\_master<br>B.id\_cliente is not null and B.id\_cliente != ''<br>B.cod\_fitir = cast(C.fccredimax\_fitir as int)<br>B.id\_pedido\_pais = 1<br>B.est\_pedido = 1 and B.ind\_credventagestora = 0 and B.ind\_reasignacion = 0<br>coalesce(B.fec\_liquidacion, B.fec\_cancelacion) is null<br>( trim(C.fcnivel\_1) in ('Prestamos Conectividad', 'Prestamos Hogar', 'Prestamos Italika', 'Prestamos Movilidad') or trim(C.fcnivel\_2) in ('Prestamos Efectivo') or trim(C.fcnivel\_3) in ('Tarjeta Azteca') ) |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT Aid\_master |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_CRYSTAL\_CREDITO |  |
|  |  |  |  |
|  | Paso 20 |  |  |
|  | Descripción | Identificación si es empleado |  |
|  | Origen Tablas Temporales | Paso 14 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_cte\_empleado\_master |  |
|  | Relación: | A.id\_master = B.id\_master<br>B.fc\_status = "ACTIVO" |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT Aid\_master |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_EMPLEADO |  |
|  |  |  |  |
|  | Paso 21 |  |  |
|  | Descripción | Identificación mes anterior |  |
|  | Origen Tablas Temporales | Paso 2 |  |
|  | Tabla A: | TEMP\_anonimato\_persona |  |
|  | Columnas Finales | cast( date\_format( add\_months( from\_unixtime( cast( max(fecharegistro)/1000 as Bigint) , "yyyy-MM-dd" ), -1 ) , "yyyyMM") as int) Num\_Periodo\_mes |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_ANTERIOR\_MES |  |
|  |  |  |  |
|  | Paso 22 |  |  |
|  | Descripción | Identificación si es Activo |  |
|  | Origen Tablas Temporales | Paso 14 y 21 |  |
|  | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla B: | cd\_baz\_bdclientes.cd\_con\_cte\_actividad\_mes |  |
|  | Tabla C: | TEMP\_ANTERIOR\_MES |  |
|  | Relación: | A.id\_master = B.id\_master<br>B.ind\_activo = 1 <br>B.Num\_Periodo\_mes = C.Num\_Periodo\_mes |  |
|  | Tipo de Unión: | inner join |  |
|  | Columnas Finales | DISTINCT A.id\_master |  |
|  | Filtro y/o condiciones | A.id\_master is not null |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_RELACION\_PERSONA\_MASTERID\_ACTIVO |  |
|  |  |  |  |
|  | Paso 23 |  |  |
|  | Descripción | Adición de marca a nivel MasterID |  |
|  | Origen Tablas Temporales | Paso 17, Paso 18, Paso 19, Paso 20 y Paso 22 |  |
| TEMP\_RELACION\_PERSONA\_MASTERID | Tabla A: | TEMP\_RELACION\_PERSONA\_MASTERID\_DIGITAL |  |
|  | Tabla B: | TEMP\_RELACION\_PERSONA\_MASTERID\_CAPTA |  |
|  | Tabla C: | TEMP\_RELACION\_PERSONA\_MASTERID\_CRYSTAL\_CREDITO |  |
|  | Tabla D: | TEMP\_RELACION\_PERSONA\_MASTERID\_EMPLEADO |  |
|  | Tabla E: | TEMP\_RELACION\_PERSONA\_MASTERID\_ACTIVO |  |
|  | Relación: | A.id\_master = B.id\_master<br>A.id\_master = C.id\_master<br>A.id\_master = D.id\_master<br>A.id\_master = E.id\_master |  |
|  | Tipo de Unión: | Left join |  |
|  | Columnas Finales | A.id\_master, A.CarcaProceso, A.clienteUnico, A.EsDigital<br> ,if(B.id\_master IS NOT NULL,1,0) as EsCaptacion<br> ,if(D.id\_master IS NOT NULL,1,0) as EsCredito<br> ,if(E.id\_master IS NOT NULL,1,0) as EsActivo<br> ,if(F.id\_master IS NOT NULL,1,0) as EsEmpleado<br> |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_MARCAS\_CLIENTE\_MASTER |  |
|  |  |  |  |
|  | Paso 24 |  |  |
|  | Descripción | Adición del Crystal de Crédito |  |
|  | Origen Tablas Temporales | Paso 10 , Paso 14 y Paso 23 |  |
| TEMP\_RELACION\_PERSONA\_MASTERID | Tabla A: | TEMP\_BASE\_EXT |  |
|  | Tabla B: | TEMP\_RELACION\_PERSONA\_MASTERID |  |
|  | Tabla C: | TEMP\_MARCAS\_CLIENTE\_MASTER |  |
|  | Relación: | A.ide = B.ide<br>A.fcnumeroeconomico = B.fcnumeroeconomico and A.identificadordocumento=B.identificadordocumento and A.fitipocanalenvid=B.fitipocanalenvid <br>B.id\_master = C.id\_master |  |
|  | Tipo de Unión: | Left join |  |
|  | Columnas Finales | DISTINCT<br> A.ide, A.fcnumeroeconomico, A.identificadordocumento, A.fitipocanalenvid <br>, A.ClienteNombre, A.ClienteNombreNexo, A.ClienteApellidoPaterno, A.ClienteApellidoNexos, A.ClienteApellidoMaterno<br>, A.nombrecompleto\_norm nombrecompletoNorm<br>, A.ClienteCorreo, A.ClienteIndicadorCorreo, A.ClienteCalificacionCorreo<br>, A.ClienteCelular, A.ClienteIndicadorCelular, A.ClienteCalifcacionCelular<br>, B.id\_master<br>, C.EsCaptacion, C.EsCredito, C.EsDigital, C.EsActivo, C.EsEmpleado, C.MarcaProceso, C.ClienteUnico |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales |  |  |
|  | Tabla Output | TEMP\_MARCAS\_CLIENTE |  |
|  |  |  |  |
|  | Paso 25 |  |  |
|  | Descripción | Tabla temporal con las base del Crystal |  |
|  | Origen Tablas Temporales | Paso 3 y Paso 24 |  |
|  | Tabla A: | TEMP\_base\_persona |  |
|  | Tabla B: | TEMP\_MARCAS\_CLIENTE |  |
|  | Relación: | A.tiendaID = B.fcnumeroeconomico, <br>A.presupuestoID = B.identificadordocumento<br>A.tipocanalid = B.fitipocanalenvid |  |
|  | Tipo de Unión: | left join |  |
|  | Columnas Finales | A.tiendaID, A.presupuestoID<br>, A.esPedido, A.ClienteUnicoPedido, A.EsPptoCredito, A.tipocanalid, A.nombretipocanal , A.banderadocumentodigital, A.banderamercadotecnia, Afecharegistro<br>, B.ClienteNombre, B.ClienteNombreNexo, B.ClienteApellidoPaterno, B.ClienteApellidoNexos, B.ClienteApellidoMaterno<br>, B.ClienteCorreo, B.ClienteIndicadorCorreo, B.ClienteCalificacionCorreo<br>, B.ClienteCelular, B.ClienteIndicadorCelular, B.ClienteCalifcacionCelular<br>, B.id\_master MasterID<br>, nvl(B.EsCaptacion,0) as EsCaptacion, nvl(B.EsCredito,0) as EsCredito, nvl(B.EsDigital,0) as EsDigital, nvl(B.esActivo as esActivo), nvl(B.EsEmpleado,0) as EsEmpleado, nvl(B.marcaProceso,0) as marcaProceso, nvl(B.clienteUnico,0) as clienteUnico <br>, if(B.id\_master is not null,1,0) as EsPersonaConocida |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tratamiento campos especiales | fechaRegistro en formato TimeStamps |  |
|  | Tabla Output | TEMP\_cd\_ekt\_prospecto\_cte\_canales\_envio\_previo\_01 |  |
|  |  |  |  |
|  | Paso 26 |  |  |
|  | Descripción | Se actualizan masterid, clienteunico e indicadores |  |
|  | Origen Tablas Temporales | Paso 25, Paso 26.1 |  |
|  | Tabla A: | TEMP\_cd\_ekt\_prospecto\_cte\_canales\_envio\_previo\_01 as cd |  |
|  | Tabla B: | TMP\_ppto as ppto |  |
|  | Tipo de Unión: | left join |  |
|  | Relación: | La relación se realiza por medio de los campos tiendaid y presupuestoid de cada tabla |  |
|  | Columnas Finales: | La selección se realiza de los registos úncos de los siguientes campos<br><br> cd.tiendaid<br>,cd.presupuestoid<br>,espedido<br>,clienteunicopedido<br>,espptocredito<br>,cd.tipocanalid<br>,cd.nombretipocanal<br>,cd.banderadocumentodigital<br>,cd.banderamercadotecnia<br>,cd.fecharegistro<br>,cd.clientenombre<br>,cd.clientenombrenexo<br>,cd.clienteapellidopaterno<br>,cd.clienteapellidonexos<br>,cd.clienteapellidomaterno<br>,cd.clientecorreo<br>,cd.clienteindicadorcorreo<br>,cd.clientecalificacioncorreo<br>,cd.clientecelular<br>,cd.clienteindicadorcelular<br>,cd.clientecalifcacioncelular |  |
|  |  | ,masterid<br>,cd.escaptacion<br>,escredito<br>,cd.esdigital<br>,cd.esactivo<br>,cd.esempleado<br>,cd.marcaproceso<br>,clienteunico<br>,espersonaconocida |  |
|  | Tratamiento campos especiales | Para el espedido, se valida si el campo ppto.espedido es igual a 1, en caso de ser cierto se asigna el valor 1, de lo contrario asigna el valor 0 <br><br>Para el clienteunicopedido, selecciona el campo ppto.clienteunico<br><br>Para el espptocredito, se valida si el campo ppto.ind\_EsPptoCredito es igual a 1, en caso de ser cierto se asigna el valor 1, de lo contrario asigna el valor 0<br><br>Para el masterid, se valida si el campo ppto.masterid es nulo, en caso de ser cierto se asigna el valor 0, de lo contrario selecciona el campo ppto.masterid<br><br>Para el escredito, valida si el ind\_escredito es igual a 1, en caso de ser cierto asigna el valor 1, de lo contrario asigna el valor 0<br><br>Para el clienteunico, valida si el campo ppto.ind\_clienteunico es igual a 1, en caso de ser cierto asigna el valor 1, de lo contrario asigna el valor 0<br><br>Para el espersonaconocida, valida si el campo ppto.masterid es mayor que 0, en caso de ser cierto asigna el valor 1, de lo contrario asigna el valor 0 |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tabla Output | cd\_ekt\_prospecto\_cte\_canales\_envio |  |
|  |  |  |  |
|  | Paso 26.1 |  |  |
|  | Descripción | Se realiza el cruce entre presupuestos únicos y pedidos únicos |  |
|  | Origen Tablas Temporales | Paso 26.1.1, Paso 26.1.2 |  |
|  | Tabla A: | TMP\_ppto1 as ppto1 |  |
|  | Tabla B: | TMP det\_pedido as det\_pedido |  |
|  | Tipo de Unión: | left join |  |
|  | Relación: | La relación se realiza entre el campo ppto1.idpedidounico de la tabla A y el campo det\_pedido.pedido\_unico de la tabla B |  |
|  | Columnas Finales: | La selección se realiza de los registos úncos de los siguientes campos<br><br> ppto1.tiendaid<br>,ppto1.presupuestoid<br>,ppto1.masterid<br>,ppto1.clienteunico<br>,ppto1.idpedidounico<br>,ppto1.espedido<br>,ind\_EsPptoCredito<br>,ind\_clienteunico<br>,ind\_escredito |  |
|  | Tratamiento campos especiales | Para el ind\_EsPptoCredito, se valida si el campo ppto1.tipoventaid es igual a 2, en caso de ser cierto se asigna el valor 1, de lo contrario asigna el valor 0<br><br>Para el ind\_clienteunico, al campo ppto1.clienteunico:<br> Si el valor original es nulo, se asigna el valor de cadena vacía<br> A la cadena resultante, se le quitan los espacios blancos a la derecha y a la izquierda<br> Si la cadena resultante es diferente a cadena vacía, asigna el valor 1, de lo contrario asigna el valor 0<br> <br>Para el ind\_escredito, valida si el campo det\_pedido.pedido\_unico es no nulo, en caso de ser cierto asigna el valor 1, de lo contrario asigna el valor 0 |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tabla Output | TMP\_ppto |  |
|  |  |  |  |
|  | Paso 26.1.1 |  |  |
|  | Descripción | Se obtienen los presupuestos únicos y sus campos principales |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cd\_ekt\_bdclientes.cd\_ekt\_prospecto\_cte\_pesupuesto |  |
|  | Columnas Finales: | La selección se realiza de los registos úncos de los siguientes campos<br><br> tiendaid<br>,presupuestoid<br>,masterid<br>,clienteunico<br>,idpedidounico<br>,espedido<br>,tipoventaid |  |
|  | Tratamiento campos especiales |  |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tabla Output | TMP\_ppto1 |  |
|  |  |  |  |
|  | Paso 26.1.2 |  |  |
|  | Descripción | Se obtienen los pédidos únicos |  |
|  | Origen Tablas Temporales |  |  |
|  | Tabla A: | cd\_baz\_bdclientes.cd\_cre\_detalle\_pedido |  |
|  | Columnas Finales: | La selección se realiza de los registos úncos de los siguientes campos<br><br>pedido\_unico |  |
|  | Tratamiento campos especiales | Para el pedido\_unico, se realiza: <br> La conversión a cadena del campo id\_pedido\_pais<br> La conversión a cadena del campo id\_pedido\_canal<br> La conversión a cadena del campo id\_pedido\_sucursal<br> La conversión a cadena del campo id\_pedido\_num <br> La concatenación de los campos anteriores, separando con guión medio cada campo |  |
|  | Filtro y/o condiciones |  |  |
|  | Reglas negocio |  |  |
|  | Tabla Output | TMP\_det\_pedido |  |
|  |  |  |  |
|  |  |  |  |
|  | Diccionario de Datos |  |  |
|  | Nombre | Nombre | Nombre |
|  | tiendaID | Número económico que pertenece a la sucursal | String |
|  | presupuestoID | Indica el número de presupuesto o ID al que pertenece el documento | String |
|  | tipocanalid | ID del tipo de canal que realiza el envio | Integer |
|  | nombretipocanal | Nombre del canal en que se realiza el envio | String |
|  | fecharegistro | Fecha en la que se envío el registro | Integer |
|  | MasterID | Indicador de persona a nivel grupo | Integer |
|  | EsPersonaConocida | Marca que permite identificar a la persona | Integer |
|  | EsCaptacion | Indicador si pertenece a la unidad de Captación | Integer |
|  | EsCredito | Indicador si pertenece a la unidad de Crédito y tiene algún pedido | Integer |
|  | EsDigital | Indicador si pertenece a la Digital | Integer |
|  | EsEmpleado | Indicador de pertenecer a empleado | Integer |
|  | esActivo | Indicador si el cliente es activo al momento de consultarse | Integer |
|  | EsPptoCredito | Indicador si el presupuesto es de crédito | Integer |
|  | esPedido | Indicador si el presupuesto se convirtio en pedido | List<String> |
|  | ClienteUnico | Cliente único asociadoMasterID por datos de la persona | Integer |
|  | ClienteUnicoPedido | Cliente único asociado al pedido que compro el cliente por una venta de crédito | Integer |
|  | banderadocumentodigital | Campo que indica la decisión de recibir documentos digitales por el cliente | Integer |
|  | banderamercadotecnia | Campo que indica la decisión de recibir campañas de marketing por el cliente | String |
|  | ClienteNombre | Nombre del cliente | String |
|  | ClienteNombreNexo | Nexoentre los nombres dell Cliente | String |
|  | ClienteApellidoPaterno | Apellido paterno que pertenece al cliente potencial | String |
|  | ClienteApellidoNexos | Nexoentre los nombres dell Cliente | String |
|  | ClienteApellidoMaterno | Apellido materno que pertenece al cliente potencial | String |
|  | ClienteCorreo | Correo electrónico que pertenece al cliente | String |
|  | ClienteIndicadorCorreo | Valor numerico de la calificación del corre del cliente | String |
|  | ClienteCalificaciónCorreo | Calificación de calidad del correo del cliente | String |
|  | ClienteCelular | Número celular que pertenece al cliente | String |
|  | ClienteIndicadorCelular | Valor numerico de la calificación del celular del cliente | String |
|  | ClienteCalifcaciónCelular | Calificación de calidad del celular del cliente |  |

## 05_CD_DER
| Unnamed: 0 | Crystal Data Diagrama Entidad Relación |
| --- | --- |

## 06_CD_Criterios_de_Aceptación
| Unnamed: 0 | Criterios de Aceptación | Unnamed: 2 |
| --- | --- | --- |
|  |  |  |
|  | Criterios de aceptación |  |
|  | No. | Descripción |
|  | 1 | La información se deberá de depositar en esquema de Crystal Data |
|  | 2 | El proceso deberá de tener una peridiocidad a nivel mensual |
|  | 3 | Deberá contemplarse a nivel prospecto |
|  |  |  |
|  |  |  |

## 07_CD_Artefactos
| Unnamed: 0 | Unnamed: 1 | Unnamed: 2 | Unnamed: 3 | Unnamed: 4 | Unnamed: 5 | Unnamed: 6 |
| --- | --- | --- | --- | --- | --- | --- |
|  | Artefactos |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  | Artefactos |  |  |  |  |  |
|  | No. | Descripción | Responsable | Medio de entrega | Peridiocidad de Entrega | Artefacto |
|  | 1 | Muestra de datos y layout final requerido | DT | Adjunto en este archivo | Única Vez |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |
|  | 2 |  |  |  |  |  |

## 08_CD_Matriz_de_Escalamiento
| Unnamed: 0 | Unnamed: 1 | Unnamed: 2 | Unnamed: 3 | Unnamed: 4 | Unnamed: 5 |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |
|  | Matriz de Escalamiento |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  | Número | Tarea | Aréa | Responsable | Contacto |
|  | 1 | Error en las ingestas | TI | Luis Gerardo Chavez Romero<br>Christopher De Jesus Ochoa Franco | luis.chavezro@elektra.com.mx<br>cochoa@algorithia.com |
|  | 2 | Error en la ejecución del Proceso | TI | Equipo Operaciones | bdfoperaciones@elektra.com.mx |
|  | 3 | Actualización reglas proceso/Error en la consistencia de los datos | Data Translators | Juan Carlos Cifuentes Durán<br>Mauricio Londoño | juan.cifuentesd@algorithia.com<br>mauricio.londonog@algorithia.com |
|  | 4 | Entendimiento de información de Negocio | Negocio | Martin Vega<br>Jose Carlos Montiel | mavega@algorithia.com<br>jose.montielm@algorithia.com |
|  | 5 | Error en datos en tablas RAW | TI Negocio | Alfa Berenice Paredes Flores | abparedes@elektra.com.mx |

## 09_CD_Glosario_de_Términos
| Unnamed: 0 | Unnamed: 1 | Unnamed: 2 |
| --- | --- | --- |
|  |  |  |
|  | Crystal Data Glosario de Términos |  |
|  |  |  |
|  | Glosario |  |
|  | Término | Descripción |

## 10_CD_Linaje
| Unnamed: 0 | Unnamed: 1 | Unnamed: 2 | Unnamed: 3 | Unnamed: 4 | Unnamed: 5 | Unnamed: 6 | Unnamed: 7 | Unnamed: 8 | Unnamed: 9 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |  |  |  |
|  | Crystal Data Linaje |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  |  |  |  |
|  | Fuente |  |  |  | Destino |  |  |  |  |
|  | Esquema | Nombre tabla | Nombre de campo | Tipo de dato | Esquema | Nombre tabla | Nombre campo | Tipo de dato | Transformación de campo |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_alta\_pedido\_estatus | id\_tienda | String |  | CU\_ELK\_AGRUPADOVENTA | TiendaID | string |  |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_alta\_pedido\_estatus | id\_tipo\_venta | Inteeger |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer | case <br> when id\_cliente= '99999' THEN 1 <br> when substring(id\_trans\_tb,1,6) in lista\_TEMP\_TAZTOR and (porce\_monto fue con tarjeta TAZ\_TOR) then 2<br> else id\_tipo\_venta <br>end)<br> |
|  |  | TEMP\_TAZTOR | codigo\_bines | String |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer | case <br> when id\_cliente= '99999' THEN 1 <br> when substring(id\_trans\_tb,1,6) in lista\_TEMP\_TAZTOR and (porce\_monto fue con tarjeta TAZ\_TOR) then 2<br> else id\_tipo\_venta <br>end)<br> |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_registra\_pago\_tb | id\_trans\_tb | String |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer | case <br> when id\_cliente= '99999' THEN 1 <br> when substring(id\_trans\_tb,1,6) in lista\_TEMP\_TAZTOR and (porce\_monto fue con tarjeta TAZ\_TOR) then 2<br> else id\_tipo\_venta <br>end)<br> |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_registra\_pago\_tb | monto | Double |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer | case <br> when id\_cliente= '99999' THEN 1 <br> when substring(id\_trans\_tb,1,6) in lista\_TEMP\_TAZTOR and (porce\_monto fue con tarjeta TAZ\_TOR) then 2<br> else id\_tipo\_venta <br>end)<br> |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_registra\_mov\_tipo\_pago | monto | Double |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer | case <br> when id\_cliente= '99999' THEN 1 <br> when substring(id\_trans\_tb,1,6) in lista\_TEMP\_TAZTOR and (porce\_monto fue con tarjeta TAZ\_TOR) then 2<br> else id\_tipo\_venta <br>end)<br> |
|  |  | CU\_ELK\_AGRUPADOVENTA | TipoVentaID | Integer |  | CU\_ELK\_AGRUPADOVENTA | TipoVenta | String | case when TipoVenta = valordellave then valoroficial end |
|  | cu\_bdsopoperlog | cu\_ebx\_catt\_baz\_tipo\_venta | valordellave | Integer |  | CU\_ELK\_AGRUPADOVENTA | TipoVenta | String | case when TipoVenta = valordellave then valoroficial end |
|  | rd\_baz\_bdclientes | rd\_mon\_201 | valoroficial | String |  | CU\_ELK\_AGRUPADOVENTA | TipoVenta | String | case when TipoVenta = valordellave then valoroficial end |
|  |  | CD\_EKT\_CATALOGO\_SKU | UnidadNegocioID | String |  | CU\_ELK\_AGRUPADOVENTA | DescripcionUnidadNegocio | string | case <br> when UnidadNegocioID in ('1','2','3') <br> then DescripcionUnidadNegocio <br>end |
|  |  | CD\_EKT\_CATALOGO\_SKU | DescripcionUnidadNegocio | String |  | CU\_ELK\_AGRUPADOVENTA | DescripcionUnidadNegocio | string | case <br> when UnidadNegocioID in ('1','2','3') <br> then DescripcionUnidadNegocio <br>end |
|  |  | CD\_EKT\_CATALOGO\_SKU | LineaID | String |  | CU\_ELK\_AGRUPADOVENTA | DescripcionLinea | string | case <br> when LineaID< 900 and LineaID NOT IN (610, 512,560, 770, 760) <br> and SKU.descor not like '%LCR%'<br> then DescripcionLinea <br>end |
|  |  | CD\_EKT\_CATALOGO\_SKU | DescripcionLinea | String |  | CU\_ELK\_AGRUPADOVENTA | DescripcionLinea | string | case <br> when LineaID< 900 and LineaID NOT IN (610, 512,560, 770, 760) <br> and SKU.descor not like '%LCR%'<br> then DescripcionLinea <br>end |
|  |  | CD\_EKT\_CATALOGO\_SKU | DescripcionSublinea | String |  | CU\_ELK\_AGRUPADOVENTA | DescripcionSublinea | string |  |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_detalle\_pedido | cantidad\_venta | double |  | CU\_ELK\_AGRUPADOVENTA | VentaPesos | Double |  |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_detalle\_pedido | cantidad\_articulos | douebl |  | CU\_ELK\_AGRUPADOVENTA | VentaUnidades | Integer |  |
|  | cu\_bdekt | cu\_ekt\_cte\_vta\_alta\_pedido\_estatus | fecha\_surtimiento | bigint |  | CU\_ELK\_AGRUPADOVENTA | Anio | string | substring(fecha\_texto(fecha\_surtimiento, "AAAAMMDD"),1,4) |
