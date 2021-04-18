---
title: Lista alfabética de todas las funciones de WCS
description: A continuación se muestra una lista alfabética completa de las funciones de la API de WCS 1,0 proporcionadas por Windows \ 160; 98 y versiones posteriores y Windows \ 160; 2000 y versiones posteriores.
ms.assetid: aba45dbd-6fc2-4788-87f0-043579fa53f9
keywords:
- Sistema de color de Windows (WCS), funciones
- WCS (sistema de colores de Windows), funciones
- Administración del color de imagen, funciones
- Administración del color, funciones
- colores, funciones
- Referencia WCS, funciones
- referencia de las funciones WCS,
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b70208c1f1f7d87b4f5cd6f4a14f3f22e0bc2f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721377"
---
# <a name="alphabetical-list-of-all-wcs-functions"></a>Lista alfabética de todas las funciones de WCS

A continuación se muestra una lista alfabética completa de las funciones de la API WCS 1,0 proporcionadas por Windows 98 y versiones posteriores, y Windows 2000 y versiones posteriores.



| Función o estructura                                                                 | Descripción                                                                                                                                          |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (o **ApplyCallbackFunction**) es una función de devolución de llamada que se implementa y que actualiza los datos de configuración de WCS mientras se está ejecutando el cuadro de diálogo que muestra la función [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) . |
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Asocia un perfil de color especificado a un dispositivo especificado.                                                                                                            |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Comprueba si los píxeles de un mapa de bits especificado se encuentran dentro de la [gama](g.md) de salida de una transformación especificada. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Determina si los colores de una matriz se encuentran dentro de la [gama](g.md) de salida de una transformación especificada. |
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                                       | Comprueba si determinados colores se encuentran en la gama de un dispositivo.                                                                                                      |
| [**CloseColorProfile**](/windows/win32/api/icm/nf-icm-closecolorprofile) | Cierra un identificador de perfil abierto. |
| [**CMCheckColors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Determina si los colores especificados se encuentran dentro de la [gama](./g.md) de salida de una transformación especificada. |
| [**CMCheckColorsInGamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Determina si los triples de RGB especificados se encuentran en la [gama](./g.md) de salida de una transformación especificada. |
| [**CMCheckRGBs**](/windows/desktop/api/Wingdi/)                                                     | Comprueba los colores del mapa de bits con una gama de salida.                                                                                                        |
| [**CMConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Convierte los nombres de colores de un espacio de colores con nombre en números de índice de un perfil de color. |
| [**CMConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Transforma índices en un espacio de colores en una matriz de nombres de un espacio de colores con nombre. |
| [**CMCreateDeviceLinkProfile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Crea un [Perfil de vínculo de dispositivo](./d.md) en el formato especificado por el consorcio de color internacional en su especificación de formato de perfil ICC. |
| [**CMCreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Acepta una matriz de perfiles o un [Perfil de vínculo de dispositivo](./d.md) único y crea una transformación de color. Esta transformación es una asignación desde el espacio de colores especificado por el primer perfil hasta el del segundo perfil, y así sucesivamente hasta el último. |
| [**CMCreateProfile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Crea un perfil de color de presentación a partir de una estructura [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) . |
| [**CMCreateProfileW**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Crea un perfil de color de presentación a partir de una estructura [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) . |
| [**CMCreateTransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | En desuso. No hay ninguna API de reemplazo porque ya no se usaba. No es necesario que los desarrolladores de módulos de CMM alternativos lo implementen. |
| [**CMCreateTransformExt**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Crea una transformación de color que se asigna desde una [**LOGCOLORSPACEA**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) de entrada a un espacio de destino opcional y, a continuación, a un dispositivo de salida, utilizando un conjunto de marcas que definen cómo se debe crear la transformación. |
| [**CMCreateTransformExtW**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Crea una transformación de color que se asigna desde una [**LOGCOLORSPACEW**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) de entrada a un espacio de destino opcional y, a continuación, a un dispositivo de salida, utilizando un conjunto de marcas que definen cómo se debe crear la transformación. |
| [**CMCreateTransformW**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | En desuso. No hay ninguna API de reemplazo porque ya no se usaba. No es necesario que los desarrolladores de módulos de CMM alternativos lo implementen. |
| [**CMDeleteTransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Elimina una transformación de color especificada y libera cualquier memoria asociada a ella. |
| [**CMGetInfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Recupera diversa información sobre el módulo de administración del color (CMM). |
| [**CMGetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Recupera información sobre el perfil de color con nombre especificado. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/)           | Obtiene un diccionario de representación de color PostScript.                                                                                                        |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Recupera el [intento de representación](rendering-intents.md) de color PostScript de nivel 2 de un perfil. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                             | Obtiene una matriz de espacio de colores PostScript.                                                                                                                 |
| [**CMIsProfileValid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Indica si el perfil determinado es un perfil ICC válido que se puede usar para la administración del color. |
| [**CMTranslateColors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Traduce una matriz de colores de un [espacio de colores](color-spaces.md) de origen a un espacio de colores de destino usando una transformación de color. |
| [**CMTranslateRGB**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Convierte un RGBQuad proporcionado por la aplicación en el espacio de [colores](color-spaces.md)del dispositivo. |
| [**CMTranslateRGBs**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Convierte un mapa de bits de un [espacio de colores](color-spaces.md) a otro usando una transformación de color. |
| [**CMTranslateRGBsExt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Convierte un mapa de bits de un formato definido a un formato definido diferente y llama periódicamente a una función de devolución de llamada, si se especifica una, para informar del progreso y permitir que la aplicación que realiza la llamada termine la traducción. |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                                     | Corrige las entradas de una paleta para un contexto de dispositivo.                                                                                              |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                                       | Realiza la asignación de colores para fines de vista previa.                                                                                                         |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Convierte los nombres de colores de un espacio de colores con nombre en números de índice en un perfil de color de International color Consortium (ICC). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transforma índices en un espacio de colores en una matriz de nombres de un espacio de colores con nombre. |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                                           | Crea un espacio de colores.                                                                                                                               |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransforma) | Transforma índices en un espacio de colores en una matriz de nombres de un espacio de colores con nombre. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transforma índices en un espacio de colores en una matriz de nombres de un espacio de colores con nombre. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Acepta una matriz de perfiles o un [Perfil de vínculo de dispositivo](d.md) único y crea una transformación de color que las aplicaciones pueden usar para realizar la asignación de colores. |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Convierte un espacio de [colores](c.md) lógico en un [Perfil de dispositivo](d.md). |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                                           | Elimina un espacio de colores.                                                                                                                               |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Elimina una transformación de color determinada. |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Desasocia un perfil de color especificado con un dispositivo especificado en un equipo especificado. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumera todos los perfiles que cumplen los criterios de enumeración especificados. |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                                             | Enumera los perfiles de color de salida disponibles para un contexto de dispositivo determinado.                                                                               |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/)                     | Función de devolución de llamada definida por la aplicación para [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).                                                                |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Recupera diversa información sobre el módulo de administración del color (CMM) que creó la transformación de color especificada. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Recupera la ruta de acceso del directorio de COLOR de Windows en un equipo especificado. |
| [**GetColorProfileElement**](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | Copia datos de un elemento de perfil etiquetado especificado de un perfil de color especificado en un búfer. |
| [**GetColorProfileElementTag**](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | Recupera el nombre de etiqueta especificado por *dwIndex* en la tabla de etiquetas de un perfil de color de International color Consortium (ICC) determinado, donde *dwIndex* es un índice basado en uno de la tabla. |
| [**GetColorProfileFromHandle**](/windows/win32/api/icm/getcolorprofilefromhandle)                         | Recupera el contenido del perfil de color dado un identificador a un perfil de color abierto.                                                                        |
| [**GetColorProfileHeader**](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | Recupera o deriva la estructura de encabezado de ICC de un perfil de color ICC o de un perfil XML WCS. Los controladores y las aplicaciones deben suponer que devolver **true** solo indica que se devuelve un encabezado estructurado correctamente. Cada etiqueta todavía tendrá que validarse de forma independiente mediante las API de ICM2 heredadas o las API de esquemas XML. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Obtiene el espacio de colores de entrada actual en un contexto de dispositivo. |
| [**GetCountColorProfileElements**](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | Recupera el número de elementos etiquetados en un perfil de color determinado. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Obtiene la rampa gamma de los paneles de presentación de colores directos.                                                                                                |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                                                 | Obtiene el perfil de color de salida actual de un contexto de dispositivo.                                                                                           |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                                           | Obtiene la estructura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) de un contexto de dispositivo.                                                                       |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Recupera información sobre el perfil de color International color Consortium (ICC) especificado en el primer parámetro. |
| [**GetPS2ColorRenderingDictionary**](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | Recupera el Diccionario de representación del color PostScript de nivel 2 del perfil de color ICC especificado. |
| [**GetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | Recupera el [intento de representación](r.md) de color PostScript de nivel 2 de un perfil de color ICC. |
| [**GetPS2ColorSpaceArray**](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | Recupera la matriz de [espacio de colores](c.md) PostScript de nivel 2 de un perfil de color ICC. |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Recupera el perfil de color registrado para el espacio de [colores](c.md)estándar especificado. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)                             | Devolución de llamada proporcionada por la aplicación para notificar el progreso.                                                                                                    |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Instala un perfil determinado para su uso en un equipo especificado. El perfil también se copia en el directorio de COLOR. |
| [**IsColorProfileTagPresent**](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | Indica si una etiqueta del consorcio de color internacional (ICC) especificada está presente en el perfil de color especificado. |
| [**IsColorProfileValid**](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | Permite determinar si el perfil especificado es un perfil de International color Consortium (ICC) válido o un identificador de perfil del sistema de colores de Windows (WCS) válido que se puede usar para la administración del color. |
| [**OpenColorProfileW**](/windows/win32/api/icm/nf-icm-opencolorprofilew) | Crea un identificador para un perfil de color especificado. El identificador se puede usar en otras funciones de administración de perfiles. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Asocia un valor de identificación especificado a la biblioteca de vínculos dinámicos del módulo de administración de color (CMM DLL) especificada. Cuando este identificador aparece en un perfil de color, Windows puede localizar la CMM correspondiente para crear una transformación. |
| [**SelectCMM**](/windows/win32/api/icm/nf-icm-selectcmm) | Permite seleccionar el módulo de administración del color preferido (CMM) que se va a usar. |
| [**SetColorProfileElement**](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | Establece los datos del elemento para un elemento de perfil etiquetado en un perfil de color de ICC. |
| [**SetColorProfileElementReference**](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | Crea en un perfil de color ICC especificado una nueva etiqueta que hace referencia a los mismos datos que una etiqueta existente. |
| [**SetColorProfileElementSize**](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | Establece el tamaño de un elemento etiquetado en un perfil de color de ICC. |
| [**SetColorProfileHeader**](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | Establece los datos de encabezado de un perfil de color ICC especificado. |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                                                 | Establece el espacio de colores de entrada de un contexto de dispositivo.                                                                                                           |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Establece la rampa gamma en los paneles de presentación de color directo.                                                                                                  |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                                       | Activa o desactiva la administración del color en un contexto de dispositivo.                                                                                                |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                                                 | Establece el perfil de color de salida para un contexto de dispositivo determinado.                                                                                            |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registra un perfil especificado para un [espacio de colores](c.md)estándar determinado. El perfil se puede consultar mediante [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew). |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                                       | Proporciona control de usuario sobre la administración del color por medio de un cuadro de diálogo.                                                                                  |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                                     | Convierte los colores del mapa de bits mediante una transformación de color.                                                                                                      |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Convierte una matriz de colores del [espacio de colores](c.md) de origen en el espacio de colores de destino, tal y como se define en una transformación de color. |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Quita un perfil de color especificado de un equipo especificado. Los archivos asociados se eliminan opcionalmente del sistema. |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Anula la Asociación de un valor de identificador especificado de una biblioteca de vínculos dinámicos (DLL CMM) determinada del módulo de administración del color. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Asocia un perfil de color WCS especificado a un dispositivo especificado.                                                                                    |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                                               | Determina si los colores de una matriz se encuentran dentro de la gama de salida de una transformación de color WCS especificada.                                            |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Convierte un perfil WCS en un perfil ICC.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Desasocia un perfil de color WCS especificado con un dispositivo especificado en un equipo especificado.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumera todos los perfiles de color que cumplen los criterios de enumeración en el ámbito de administración de perfiles especificado.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize) | Devuelve el tamaño, en bytes, del búfer requerido por la función [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) para enumerar los perfiles de color. |
| [**WcsGetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | Determina si la administración del sistema del estado de calibración de pantalla está habilitada.                                                                    |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) | Recupera el perfil de color predeterminado para un dispositivo o el valor predeterminado independiente del dispositivo si no se especifica el dispositivo.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Devuelve el tamaño, en bytes, del nombre de Perfil de color predeterminado para un dispositivo, incluido el terminador **null** .                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Devuelve el usuario o el intento de representación en todo el sistema.                                                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Determina si el usuario ha elegido utilizar una lista de asociaciones de perfil por usuario para el dispositivo especificado.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Crea un identificador para un perfil de color especificado.                                                                                                       |
| [**WcsSetCalibrationManagementState**](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | Habilita o deshabilita la administración del sistema del estado de calibración de la pantalla.                                                                              |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Establece el nombre de Perfil de color predeterminado del tipo de perfil especificado en el ámbito de administración de perfiles especificado.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Establece el intento de representación en todo el sistema o el usuario.                                                                                                       |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Permite al usuario especificar si se va a utilizar o no una lista de asociaciones de perfil por usuario para el dispositivo especificado.                                       |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Convierte una matriz de colores del espacio de colores de origen en el espacio de colores de destino, tal y como se define en una transformación de color.                            |



 

 

 