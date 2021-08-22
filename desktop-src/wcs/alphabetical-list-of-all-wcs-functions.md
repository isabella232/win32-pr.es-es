---
title: Lista alfabética de todas las funciones de WCS
description: A continuación se muestra una lista alfabética completa de las funciones de API wcs 1.0 proporcionadas por Windows \ 160;98 y versiones posteriores y Windows \ 160;2000 y versiones posteriores.
ms.assetid: aba45dbd-6fc2-4788-87f0-043579fa53f9
keywords:
- Windows Sistema de colores (WCS), funciones
- WCS (Windows Color System),functions
- administración de colores de imagen, funciones
- administración de colores, funciones
- colors,functions
- WCS reference,functions
- referencia de WCS,functions
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e2c9250cc9fb1e9e418079ed3b9524b3add2535dd780eed65ae998bda80ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706665"
---
# <a name="alphabetical-list-of-all-wcs-functions"></a>Lista alfabética de todas las funciones de WCS

A continuación se muestra una lista alfabética completa de las funciones de API de WCS 1.0 proporcionadas por Windows 98 y versiones posteriores y Windows 2000 y versiones posteriores.



| Función o estructura                                                                 | Descripción                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (o **ApplyCallbackFunction**) es una función de devolución de llamada que se implementa que actualiza los datos de configuración de WCS mientras se ejecuta el cuadro de diálogo que muestra la función [**SetupColorMatchingW.**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) |
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Asocia un perfil de color especificado a un dispositivo especificado.                                                                                                            |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Comprueba si los píxeles de un mapa de bits especificado se encuentran dentro de la [gama de salida](g.md) de una transformación especificada. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina si los colores de una matriz se encuentran dentro de la [gama de salida](g.md) de una transformación especificada. |
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                                       | Comprueba si los colores dados están en la gama de un dispositivo.                                                                                                      |
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Cierra un identificador de perfil abierto. |
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Determina si los colores especificados se encuentran dentro de la [gama de salida](./g.md) de una transformación especificada. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Determina si los triples RGB especificados se encuentran en la [gama de salida](./g.md) de una transformación especificada. |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                                     | Comprueba los colores del mapa de bits con una gama de salida.                                                                                                        |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Convierte los nombres de color de un espacio de colores con nombre en números de índice en un perfil de color. |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Transforma los índices de un espacio de colores en una matriz de nombres en un espacio de colores con nombre. |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Crea un [perfil de vínculo de dispositivo](./d.md) en el formato especificado por International Color Consortium en su especificación de formato de perfil DEIA. |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Acepta una matriz de perfiles o un único perfil [de vínculo de dispositivo](./d.md) y crea una transformación de color. Esta transformación es una asignación del espacio de color especificado por el primer perfil al del segundo perfil, y así sucesivamente al último. |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Crea un perfil de color para mostrar a partir [**de una estructura LOGCOLORSPACEA.**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Crea un perfil de color para mostrar a partir [**de una estructura LOGCOLORSPACEW.**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | En desuso. No hay ninguna API de reemplazo porque ya no se usaba esta. No es necesario que los desarrolladores de módulos CMM alternativos lo implementen. |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Crea una transformación de color que se asigna desde una [**entrada LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) a un espacio de destino opcional y, a continuación, a un dispositivo de salida, mediante un conjunto de marcas que definen cómo se debe crear la transformación. |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Crea una transformación de color que se asigna desde una [**entrada LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) a un espacio de destino opcional y, a continuación, a un dispositivo de salida, mediante un conjunto de marcas que definen cómo se debe crear la transformación. |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | En desuso. No hay ninguna API de reemplazo porque ya no se usaba esta. No es necesario que los desarrolladores de módulos CMM alternativos lo implementen. |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Elimina una transformación de color especificada y libera cualquier memoria asociada a ella. |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Recupera diversas información sobre el módulo de administración de colores (CMM). |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Recupera información sobre el perfil de color con nombre especificado. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/)           | Obtiene un diccionario PostScript de representación de color.                                                                                                        |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Recupera la intención de PostScript de color de nivel 2 [de](rendering-intents.md) un perfil. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                             | Obtiene una matriz PostScript de espacio de colores.                                                                                                                 |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Informa de si el perfil dado es un perfil DE LAN válido que se puede usar para la administración de colores. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Convierte una matriz de colores de un espacio [de colores de origen](color-spaces.md) a un espacio de colores de destino mediante una transformación de color. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Convierte un RGBQuad proporcionado por la aplicación en el espacio [de color del dispositivo.](color-spaces.md) |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Convierte un mapa de bits de un [espacio de colores](color-spaces.md) a otro mediante una transformación de color. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Convierte un mapa de bits de un formato definido en un formato definido diferente y llama a una función de devolución de llamada periódicamente, si se especifica una, para notificar el progreso y permitir que la aplicación que realiza la llamada finalice la traducción. |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                                     | Corrige las entradas de una paleta para un contexto de dispositivo.                                                                                              |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                                       | Realiza la asignación de colores con fines de vista previa.                                                                                                         |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Convierte los nombres de color de un espacio de colores con nombre en números de índice en un perfil de color de International Color Consortium (DOW). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transforma los índices de un espacio de colores en una matriz de nombres en un espacio de colores con nombre. |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                                           | Crea un espacio de colores.                                                                                                                               |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransforma) | Transforma los índices de un espacio de colores en una matriz de nombres en un espacio de colores con nombre. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transforma los índices de un espacio de colores en una matriz de nombres en un espacio de colores con nombre. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Acepta una matriz de perfiles o un perfil de vínculo de dispositivo único y crea una transformación de color que las aplicaciones pueden usar para realizar la asignación de colores. [](d.md) |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Convierte un espacio [de color lógico en](c.md) un perfil de [dispositivo.](d.md) |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                                           | Elimina un espacio de colores.                                                                                                                               |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Elimina una transformación de color determinada. |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Desasocia un perfil de color especificado con un dispositivo especificado en un equipo especificado. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumera todos los perfiles que cumplen los criterios de enumeración especificados. |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                                             | Enumera los perfiles de color de salida disponibles para un contexto de dispositivo determinado.                                                                               |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/)                     | Función de devolución de llamada definida por la aplicación [**para EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).                                                                |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera diversas información sobre el módulo de administración de colores (CMM) que creó la transformación de color especificada. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Recupera la ruta de acceso del Windows color en un equipo especificado. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia los datos de un elemento de perfil etiquetado especificado de un perfil de color especificado en un búfer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera el nombre de etiqueta especificado por *dwIndex* en la tabla de etiquetas de un perfil de color determinado de International Color Consortium (DOW), donde *dwIndex* es un índice basado en uno en esa tabla. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/getcolorprofilefromhandle)                         | Recupera el contenido del perfil de color dado un identificador a un perfil de color abierto.                                                                        |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera o deriva la estructura de encabezados DE LA PROPIEDAD a partir del perfil de color DE LA FILA o del perfil XML de WCS. Los controladores y las aplicaciones deben asumir que devolver **TRUE** solo indica que se devuelve un encabezado estructurado correctamente. Cada etiqueta tendrá que validarse de forma independiente mediante las API ICM2 heredadas o las API de esquema XML. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Obtiene el espacio de color de entrada actual en un contexto de dispositivo. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera el número de elementos etiquetados en un perfil de color determinado. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Obtiene la rampa gamma de los paneles de visualización de color directo.                                                                                                |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                                                 | Obtiene el perfil de color de salida actual de un contexto de dispositivo.                                                                                           |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                                           | Obtiene la [**estructura LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) de un contexto de dispositivo.                                                                       |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera información sobre el perfil de color con nombre de International Color Consortium (ICC) que se especifica en el primer parámetro. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera el diccionario de PostScript de representación de colores de nivel 2 del perfil de color DE LAN especificado. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera la intención de PostScript de [color](r.md) nivel 2 de un perfil de color DE COLOR DE COLOR DE NIVEL 2. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera la matriz PostScript espacio [de colores](c.md) nivel 2 de un perfil de color DE COLOR DE NIVEL 2. |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Recupera el perfil de color registrado para el espacio de [colores estándar especificado.](c.md) |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)                             | Devolución de llamada proporcionada por la aplicación para informar del progreso.                                                                                                    |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Instala un perfil determinado para su uso en un equipo especificado. El perfil también se copia en el directorio COLOR. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Indica si una etiqueta especificada de International Color Consortium (ICC) está presente en el perfil de color especificado. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Permite determinar si el perfil especificado es un perfil válido de International Color Consortium (ICC) o un identificador de perfil válido de Windows Color System (WCS) que se puede usar para la administración de colores. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Crea un identificador para un perfil de color especificado. A continuación, el identificador se puede usar en otras funciones de administración de perfiles. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Asocia un valor de identificación especificado a la biblioteca de vínculos dinámicos (DLL de CMM) del módulo de administración de colores especificado. Cuando este identificador aparece en un perfil de color, Windows buscar la CMM correspondiente para crear una transformación. |
| [**SeleccioneCMM.**](/windows/win32/api/icm/nf-icm-selectcmm) | Permite seleccionar el módulo de administración de colores (CMM) preferido que se va a usar. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Establece los datos del elemento para un elemento de perfil etiquetado en un perfil de color DE COLOR DE COLOR. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Crea en un perfil de color DE LAN especificado una nueva etiqueta que hace referencia a los mismos datos que una etiqueta existente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Establece el tamaño de un elemento etiquetado en un perfil de color DECTE. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Establece los datos de encabezado en un perfil de color DE LAN especificado. |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                                                 | Establece el espacio de color de entrada de un contexto de dispositivo.                                                                                                           |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Establece la rampa gamma en los paneles de visualización de color directo.                                                                                                  |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                                       | Activa o desactiva la administración de colores en un contexto de dispositivo.                                                                                                |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                                                 | Establece el perfil de color de salida para un contexto de dispositivo determinado.                                                                                            |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registra un perfil especificado para un espacio de [color estándar determinado.](c.md) El perfil se puede consultar mediante [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew). |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                                       | Proporciona control de usuario sobre la administración de colores mediante un cuadro de diálogo.                                                                                  |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                                     | Convierte los colores de mapa de bits mediante una transformación de color.                                                                                                      |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Convierte una matriz de colores del espacio [de colores de origen](c.md) al espacio de colores de destino, tal como se define en una transformación de color. |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Quita un perfil de color especificado de un equipo especificado. Opcionalmente, los archivos asociados se eliminan del sistema. |
| [**Anulación del registroCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Desasocia un valor de identificador especificado de una biblioteca de vínculos dinámicos (DLL de CMM) del módulo de administración de colores determinado. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Asocia un perfil de color WCS especificado a un dispositivo especificado.                                                                                    |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                                               | Determina si los colores de una matriz se encuentran dentro de la gama de salida de una transformación de color WCS especificada.                                            |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Convierte un perfil WCS en un perfil DE LAN.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Desasocia un perfil de color WCS especificado con un dispositivo especificado en un equipo especificado.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumera todos los perfiles de color que cumplen los criterios de enumeración en el ámbito de administración de perfiles especificado.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) | Devuelve el tamaño, en bytes, del búfer requerido por la función [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) para enumerar los perfiles de color. |
| [**WcsGetGetGetbrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina si la administración del sistema del estado de calibración de pantalla está habilitada.                                                                    |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) | Recupera el perfil de color predeterminado para un dispositivo o el valor predeterminado independiente del dispositivo si no se especifica el dispositivo.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Devuelve el tamaño, en bytes, del nombre del perfil de color predeterminado para un dispositivo, incluido el terminador **NULL.**                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Devuelve la intención de representación de usuario o de todo el sistema.                                                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Determina si el usuario ha elegido usar una lista de asociaciones de perfil por usuario para el dispositivo especificado.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Crea un identificador para un perfil de color especificado.                                                                                                       |
| [**WcsSetIntegrabrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Habilita o deshabilita la administración del sistema del estado de calibración de la pantalla.                                                                              |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Establece el nombre del perfil de color predeterminado del tipo de perfil especificado en el ámbito de administración de perfiles especificado.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Establece la intención de representación de usuario o de todo el sistema.                                                                                                       |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Permite al usuario especificar si se debe usar o no una lista de asociaciones de perfil por usuario para el dispositivo especificado.                                       |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Traduce una matriz de colores del espacio de colores de origen al espacio de color de destino, tal como se define en una transformación de color.                            |



 

 

 