---
description: Compatibilidad con la reproducción automática
ms.assetid: e91334d9-9041-4cb8-a6d0-0e2371800064
title: Compatibilidad con la reproducción automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83091191d8468b7ea3d34146e4a4c02e8cf5bf80cb3e49c72dc43bb092d10f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083399"
---
# <a name="supporting-autoplay"></a>Compatibilidad con la reproducción automática

Reproducción automática es una característica del Shell que inicia aplicaciones asociadas a dispositivos determinados. En función de la configuración actual de Reproducción automática, esta característica realizará una de varias acciones, como presentar una lista de aplicaciones de controlador disponibles, mostrar una vista de carpeta estándar de archivos, y así sucesivamente.

En Windows Vista, la característica Reproducción automática se extendió para que un dispositivo WPD pueda proporcionar una lista de tipos de contenido que admite. De forma similar, las aplicaciones WPD pueden registrar los tipos de contenido que admiten. Por ejemplo, un asistente para adquisición de fotos puede registrarse como controlador para cualquier dispositivo WPD que proporciona imágenes, y una aplicación multimedia puede registrarse como controlador para cualquier dispositivo que almacena archivos de audio o vídeo.

Las aplicaciones registran información específica del controlador escribiendo entradas en la clave **HKEY \_ LOCAL MACHINE SOFTWARE de Microsoft Windows controladores \_ \\ \\ \\ \\ \\ \\ autoplayHandlers \\ del Explorador de CurrentVersion.** Con un controlador de aplicación WPD (denominado MyWpdApplication.exe) como ejemplo, la aplicación puede insertar los valores siguientes en una clave **\\ \\ Handlers MyWpdApplicationHandler.**



| Valor          | Tipo            | Datos                                                 |
|----------------|-----------------|------------------------------------------------------|
| Acción         | REG \_ SZ         | Examinar contenido en dispositivos portátiles.                  |
| CLSIDForCancel | REG \_ SZ         | {00000000-0000-0000-0000-000000000000}               |
| DefaultIcon    | REG \_ EXPAND \_ SZ | %SystemDrive% \\ multimedia \\ wpd \\MyWpdApplication.exe |
| InitCmdLine    | REG \_ SZ         | /AutoPlay                                            |
| ProgID         | REG \_ SZ         | MyWpdApplication.MyWpdApplicationAutoPlay            |
| Proveedor       | REG \_ SZ         | MyWpdApplication                                     |



 

Para obtener más información sobre las claves y los valores del Registro de Reproducción automática que se encuentran en la clave **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Explorer \\ \\ AutoplayHandlers \\ Handlers** , consulte la documentación correspondiente en MSDN.

### <a name="the-wpd-autoplay-scheme"></a>Esquema de reproducción automática de WPD

El esquema de reproducción automática de WPD se integra con la Windows Vista AutoPlay. Para ello, admite tres categorías de reproducción automática, que se describen en la tabla siguiente.



| Categoría | Descripción                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------|
| Source   | Un dispositivo WPD se puede tratar como un origen de contenido (es decir, el contenido se puede transferir desde el dispositivo).        |
| Receptor     | Un dispositivo WPD se puede tratar como destino del contenido (es decir, el contenido se puede transferir al dispositivo).    |
| Función | Un dispositivo WPD admite una funcionalidad programable o controlable (por ejemplo, puede enviar y recibir mensajes SMS). |



 

Las aplicaciones se registran para la categoría de origen, receptor o función adecuada escribiendo entradas en la sección Reproducción automática del registro del sistema. Estas entradas aparecen bajo la clave **WPD HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Explorer \\ \\ AutoplayHandlers \\ EventHandlers. \\** En la clave WPD se encuentran las **claves Function**, **Sink** **y Source.** En cada una de estas claves hay un GUID que corresponde a una categoría funcional o un tipo de contenido de WPD.

En la tabla siguiente se enumeran  los GUID que se encuentran en la clave de función del Registro e identifica la categoría funcional que corresponde a cada GUID.



| Categoría funcional de WPD                           | Clave del Registro (GUID)                    |
|---------------------------------------------------|----------------------------------------|
| CATEGORÍA FUNCIONAL DE WPD \_ \_ \_ ALL                    | {2D8A6512-A74C-448E-BA8A-F4AC07C49399} |
| CAPTURA DE AUDIO \_ DE CATEGORÍA FUNCIONAL DE \_ \_ \_ WPD         | {3F2A1919-C7C2-4A00-855D-F57CF06DEBBB} |
| DISPOSITIVO DE CATEGORÍA \_ FUNCIONAL \_ \_ WPD                 | {08EA466B-E3A4-4336-A1F3-A44D2B5C438C} |
| CONFIGURACIÓN DE RED \_ DE \_ CATEGORÍA FUNCIONAL \_ DE \_ WPD | {48F4DB72-7C6A-4AB0-9E1A-470E3CDBF26A} |
| INFORMACIÓN DE REPRESENTACIÓN \_ DE \_ CATEGORÍAS FUNCIONALES DE \_ \_ WPD | {08600BA4-A7BA-4A01-AB0E-0065D0A356D3} |
| SMS DE CATEGORÍA \_ FUNCIONAL \_ DE \_ WPD                    | {0044A0B1-C1E9-4AFD-B358-A62C6117C9CF} |
| CAPTURA DE IMÁGENES \_ DE LA CATEGORÍA FUNCIONAL \_ \_ DE \_ \_ WPD  | {613CA327-AB93-4900-B4FA-895BB5874B79} |
| ALMACENAMIENTO DE CATEGORÍAS \_ \_ FUNCIONALES DE \_ WPD                | {23F05BBC-15DE-4C2A-A55B-A9AF5CE412EF} |
| CAPTURA DE VÍDEO \_ DE CATEGORÍA FUNCIONAL DE \_ \_ \_ WPD         | {E23E5F6B-7243-43AA-8DF1-0EB3D968A918} |



 

En la tabla siguiente se enumeran los GUID que se encuentran en las claves **Sink** y **Source** del Registro e identifica el tipo de contenido que corresponde a cada GUID.



| Tipo de contenido DE WPD                          | Clave del Registro (GUID)                    |
|-------------------------------------------|----------------------------------------|
| TIPO DE \_ CONTENIDO WPD \_ \_ ALL                   | {80E170D2-1055-4A3E-B952-82CC4F8A8689} |
| CITA DE TIPO \_ DE \_ CONTENIDO WPD \_           | {0FED060E-8793-4B1E-90C9-48AC389AC631} |
| AUDIO DE \_ TIPO \_ DE CONTENIDO WPD \_                 | {4AD2C85E-5E2D-45E5-8864-4F229E3C6CF0} |
| WPD \_ CONTENT \_ TYPE \_ AUDIO \_ ALBUM          | {AA18737E-5009-48FA-AE21-85F24383B4E6} |
| CALENDARIO DE TIPO \_ DE \_ CONTENIDO DE \_ WPD              | {A1FD5967-6023-49A0-9DF1-F8060BE751B0} |
| CERTIFICADO DE TIPO \_ DE \_ CONTENIDO \_ WPD           | {DC3876E8-A948-4060-9050-CDC77E8A3D87} |
| CONTACTO DE TIPO \_ \_ DE CONTENIDO WPD \_               | {EABA8313-4525-4707-9F0E-87C6808E9435} |
| GRUPO DE CONTACTOS \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD        | {346B8932-4C36-40D8-9415-1828291F9DE9} |
| DOCUMENTO DE \_ TIPO DE CONTENIDO DE \_ \_ WPD              | {680ADF52-950A-4041-9B41-65E393648155} |
| CORREO ELECTRÓNICO DE \_ TIPO DE CONTENIDO DE \_ \_ WPD                 | {8038044A-7E51-4F8F-883D-1D0623D14533} |
| CARPETA DE TIPO \_ DE \_ CONTENIDO DE \_ WPD                | {27E2E392-A111-48E0-AB0C-E17705A05F85} |
| OBJETO FUNCIONAL \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD    | {99ED0160-17FF-4C44-9D98-1D7A6F941921} |
| ARCHIVO GENÉRICO \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD         | {0085E0A6-8D34-45D7-BC5C-447E59C73D48} |
| MENSAJE GENÉRICO \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD      | {E80EAAF8-B2DB-4133-B67E-1BEF4B4A6E5F} |
| IMAGEN DE TIPO \_ DE \_ CONTENIDO \_ WPD                 | {EF2107D5-A52A-4243-A26B-62D4176D7603} |
| WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM          | {75793148-15F5-4A30-A813-54ED8A37E226} |
| CONVERSIÓN MULTIMEDIA \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD           | {5E88B3CC-3E65-4E62-BFFF-229495253AB0} |
| WPD \_ CONTENT \_ TYPE \_ MEMO                  | {9CD20ECF-3B50-414F-A641-E473FFE45751} |
| WPD \_ CONTENT \_ TYPE \_ MIXED \_ CONTENT \_ ALBUM | {00F0C3AC-A593-49AC-9219-24ABCA5A2563} |
| ASOCIACIÓN DE RED \_ DEL TIPO DE CONTENIDO \_ \_ \_ WPD  | {031DA7EE-18C8-4205-847E-89A11261D0F3} |
| LISTA DE REPRODUCCIÓN \_ DE TIPO DE CONTENIDO \_ \_ WPD              | {1A33F7E4-AF13-48F5-994E-77369DFE04A3} |
| PROGRAMA DE TIPO \_ DE \_ CONTENIDO \_ WPD               | {D269F96A-247C-4BFF-98FB-97F3C49220E6} |
| SECCIÓN TIPO DE \_ CONTENIDO \_ \_ WPD               | {821089F5-1D91-4DC9-BE3C-BBB1B35B18CE} |
| TAREA TIPO \_ DE \_ CONTENIDO \_ WPD                  | {63252F2C-887F-4CB6-B1AC-D29855DCEF6C} |
| WPD \_ CONTENT \_ TYPE \_ TV            | {60A169CF-F2AE-4E21-9375-9677F11C1C6E} |
| TIPO DE \_ CONTENIDO \_ WPD \_ SIN ESPECIFICAR           | {28D8D31E-249C-454E-AABC-34883168E634} |
| VÍDEO DE \_ TIPO DE \_ CONTENIDO \_ WPD                 | {9261B03C-3D78-4519-85E3-02C5E1F50BB9} |
| WPD \_ CONTENT \_ TYPE \_ VIDEO \_ ALBUM          | {012B0DB7-D4C1-45D6-B081-94B87779614F} |
| PERFIL INALÁMBRICO \_ DE TIPO DE CONTENIDO \_ \_ \_ WPD     | {0BAC070A-9F5F-4DA4-A8F6-3DE44D68FD6C} |



 

Si una aplicación admite una determinada función, origen o categoría de receptor, insertaría una cadena que especifica el nombre de la clave de controlador en el GUID que identificó la categoría funcional o de tipo de contenido admitida. Con MyWpdApplication como ejemplo, la aplicación crearía una entrada en ... **/EventHandlers/WPD/Function**, **o /Sink** o **/Source** keys. Esta entrada tendría el formato "MyWpdApplicationHandler" y sería de tipo REG \_ SZ. Además, esta entrada aparecería bajo el GUID para las categorías funcionales o los tipos de contenido que admite la aplicación.

 

 



