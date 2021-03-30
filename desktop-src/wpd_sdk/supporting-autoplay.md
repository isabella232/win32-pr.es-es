---
description: Compatibilidad con la reproducción automática
ms.assetid: e91334d9-9041-4cb8-a6d0-0e2371800064
title: Compatibilidad con la reproducción automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467a4f6289492177beab0469a181297b13accfce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816299"
---
# <a name="supporting-autoplay"></a>Compatibilidad con la reproducción automática

La reproducción automática es una característica del shell que inicia las aplicaciones asociadas a determinados dispositivos. Dependiendo de la configuración actual de reproducción automática, esta característica realizará una de varias acciones, como presentar una lista de aplicaciones de controlador disponibles, mostrar una vista de carpeta estándar de archivos, etc.

En Windows Vista, la característica reproducción automática se amplió para que un dispositivo WPD pueda proporcionar una lista de tipos de contenido que admite. Del mismo modo, las aplicaciones de WPD pueden registrar los tipos de contenido que admiten. Por ejemplo, un asistente de adquisición fotográfica puede registrarse como controlador para cualquier dispositivo de WPD que proporcione imágenes, y una aplicación multimedia puede registrarse como controlador de cualquier dispositivo que almacene archivos de audio o vídeo.

Las aplicaciones registran información específica del controlador escribiendo entradas en la clave **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ handlers** . Mediante el uso de un controlador de aplicación de WPD (denominado MyWpdApplication.exe) como ejemplo, la aplicación puede insertar los valores siguientes en una clave **\\ \\ MyWpdApplicationHandler de controladores** .



| Value          | Tipo            | Datos                                                 |
|----------------|-----------------|------------------------------------------------------|
| Acción         | Registro \_ SZ         | Examinar contenido en dispositivos portátiles.                  |
| CLSIDForCancel | Registro \_ SZ         | {00000000-0000-0000-0000-000000000000}               |
| DefaultIcon    | REG \_ expandir \_ SZ | % SystemDrive% \\ multimedia \\ WPD \\MyWpdApplication.exe |
| InitCmdLine    | Registro \_ SZ         | /AutoPlay                                            |
| ProgID         | Registro \_ SZ         | MyWpdApplication.MyWpdApplicationAutoPlay            |
| Proveedor       | Registro \_ SZ         | MyWpdApplication                                     |



 

Para obtener más información acerca de las claves y los valores del registro de reproducción automática que se encuentran en la clave **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AUTOPLAYHANDLERS \\ handlers** , consulte la documentación correspondiente en MSDN.

### <a name="the-wpd-autoplay-scheme"></a>El esquema de reproducción automática de WPD

El esquema de reproducción automática de WPD se integra con la característica de reproducción automática de Windows Vista. Para ello, admite tres categorías de reproducción automática, que se describen en la tabla siguiente.



| Category | Descripción                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------|
| Source   | Un dispositivo WPD se puede tratar como un origen de contenido (es decir, el contenido se puede transferir desde el dispositivo).        |
| Receptor     | Un dispositivo WPD se puede tratar como destino del contenido (es decir, el contenido se puede transferir al dispositivo).    |
| Función | Un dispositivo WPD admite una funcionalidad programable o controlable (por ejemplo, puede enviar y recibir mensajes SMS). |



 

Las aplicaciones se registran para la categoría de origen, receptor o función adecuada escribiendo entradas en la sección reproducción automática del registro del sistema. Estas entradas aparecen en la clave **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ AutoplayHandlers \\ EventHandlers \\ WPD** . En la clave de WPD se encuentran la **función**, el **receptor** y las claves de **origen** . En cada una de estas claves se encuentra un GUID que corresponde a un tipo de contenido o una categoría funcional de WPD.

En la tabla siguiente se enumeran los GUID que se encuentran en la clave de **función** del registro y se identifica la categoría funcional que corresponde a cada GUID.



| Categoría funcional de WPD                           | Clave del registro (GUID)                    |
|---------------------------------------------------|----------------------------------------|
| \_categoría funcional \_ \_ todo en WPD                    | {2D8A6512-A74C-448E-BA8A-F4AC07C49399} |
| \_captura de \_ audio de categoría funcional \_ de WPD \_         | {3F2A1919-C7C2-4A00-855D-F57CF06DEBBB} |
| \_dispositivo de \_ categoría \_ funcional de WPD                 | {08EA466B-E3A4-4336-A1F3-A44D2B5C438C} |
| \_configuración de \_ red de categoría funcional \_ de WPD \_ | {48F4DB72-7C6A-4AB0-9E1A-470E3CDBF26A} |
| \_información de \_ representación de categoría funcional \_ de WPD \_ | {08600BA4-A7BA-4A01-AB0E-0065D0A356D3} |
| \_SMS de \_ categoría \_ funcional de WPD                    | {0044A0B1-C1E9-4AFD-B358-A62C6117C9CF} |
| \_captura de \_ imagen de categoría funcional de \_ WPD \_ \_  | {613CA327-AB93-4900-B4FA-895BB5874B79} |
| \_almacenamiento de \_ categoría \_ funcional de WPD                | {23F05BBC-15DE-4C2A-A55B-A9AF5CE412EF} |
| \_captura de \_ vídeo de categoría funcional \_ de WPD \_         | {E23E5F6B-7243-43AA-8DF1-0EB3D968A918} |



 

En la tabla siguiente se enumeran los GUID que se encuentran en el **receptor** y las claves de **origen** del registro, y se identifica el tipo de contenido que corresponde a cada GUID.



| Tipo de contenido de WPD                          | Clave del registro (GUID)                    |
|-------------------------------------------|----------------------------------------|
| tipo de contenido de WPD \_ \_ \_ todo                   | {80E170D2-1055-4A3E-B952-82CC4F8A8689} |
| \_cita de \_ tipo de contenido de WPD \_           | {0FED060E-8793-4B1E-90C9-48AC389AC631} |
| tipo de contenido de WPD ( \_ \_ \_ audio)                 | {4AD2C85E-5E2D-45E5-8864-4F229E3C6CF0} |
| tipo de contenido de WPD \_ \_ \_ álbum de audio \_          | {AA18737E-5009-48FA-AE21-85F24383B4E6} |
| \_calendario de \_ tipo de contenido de WPD \_              | {A1FD5967-6023-49A0-9DF1-F8060BE751B0} |
| \_certificado de \_ tipo de contenido de WPD \_           | {DC3876E8-A948-4060-9050-CBD77E8A3D87} |
| \_contacto del \_ tipo de contenido de WPD \_               | {EABA8313-4525-4707-9F0E-87C6808E9435} |
| \_grupo de \_ contactos de tipo de contenido de WPD \_ \_        | {346B8932-4C36-40D8-9415-1828291F9DE9} |
| \_documento de \_ tipo de contenido de WPD \_              | {680ADF52-950A-4041-9B41-65E393648155} |
| \_ \_ correo electrónico de tipo de contenido de WPD \_                 | {8038044A-7E51-4F8F-883D-1D0623D14533} |
| \_carpeta de \_ tipo de contenido de WPD \_                | {27E2E392-A111-48E0-AB0C-E17705A05F85} |
| \_ \_ objeto funcional de tipo de contenido de \_ WPD \_    | {99ED0160-17FF-4C44-9D98-1D7A6F941921} |
| \_ \_ archivo genérico de tipo de contenido de \_ WPD \_         | {0085E0A6-8D34-45D7-BC5C-447E59C73D48} |
| \_ \_ mensaje genérico de tipo de contenido de \_ WPD \_      | {E80EAAF8-B2DB-4133-B67E-1BEF4B4A6E5F} |
| \_imagen de \_ tipo de contenido de WPD \_                 | {EF2107D5-A52A-4243-A26B-62D4176D7603} |
| \_álbum de \_ imagen del tipo de contenido de WPD \_ \_          | {75793148-15F5-4A30-A813-54ED8A37E226} |
| \_conversión de \_ multimedia de tipo de contenido de WPD \_ \_           | {5E88B3CC-3E65-4E62-BFFF-229495253AB0} |
| tipo de contenido de WPD, \_ \_ \_ memorando                  | {9CD20ECF-3B50-414F-A641-E473FFE45751} |
| \_álbum de \_ \_ contenido mixto \_ de tipo de contenido de \_ WPD | {00F0C3AC-A593-49AC-9219-24ABCA5A2563} |
| \_Asociación de \_ red del tipo de contenido de WPD \_ \_  | {031DA7EE-18C8-4205-847E-89A11261D0F3} |
| \_lista de \_ reproducción de tipo de contenido de WPD \_              | {1A33F7E4-AF13-48F5-994E-77369DFE04A3} |
| \_programa de \_ tipo de contenido de WPD \_               | {D269F96A-247C-4BFF-98FB-97F3C49220E6} |
| \_sección de \_ tipo de contenido de WPD \_               | {821089F5-1D91-4DC9-BE3C-BBB1B35B18CE} |
| tipo de contenido de WPD, \_ \_ \_ tarea                  | {63252F2C-887F-4CB6-B1AC-D29855DCEF6C} |
| \_ \_ televisor tipo de contenido de WPD \_            | {60A169CF-F2AE-4E21-9375-9677F11C1C6E} |
| tipo de contenido de WPD no \_ \_ \_ especificado           | {28D8D31E-249C-454E-AABC-34883168E634} |
| vídeo sobre el tipo de contenido de WPD \_ \_ \_                 | {9261B03C-3D78-4519-85E3-02C5E1F50BB9} |
| tipo de contenido de WPD \_ \_ \_ álbum de vídeo \_          | {012B0DB7-D4C1-45D6-B081-94B87779614F} |
| \_ \_ perfil inalámbrico de tipo de contenido de \_ WPD \_     | {0BAC070A-9F5F-4DA4-A8F6-3DE44D68FD6C} |



 

Si una aplicación admite una determinada función, origen o categoría de receptor, insertaría una cadena que especifica el nombre de la clave de controlador en el GUID que identificó la categoría funcional o de tipo de contenido compatible. Mediante MyWpdApplication como ejemplo, la aplicación crearía una entrada en... Claves **/EventHandlers/WPD/function**, o **/Sink** o **/source** . Esta entrada tendría el formato "MyWpdApplicationHandler" y ser de tipo REG \_ SZ. Además, esta entrada aparecería debajo del GUID para las categorías funcionales o los tipos de contenido que admite la aplicación.

 

 



