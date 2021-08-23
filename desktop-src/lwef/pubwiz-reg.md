---
title: Registro de un servicio
description: Para agregar el servicio a la lista de proveedores en el Asistente para publicación web o en el Asistente para ordenación de impresión en línea, debe agregar la clave adecuada y sus valores al Windows web.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- register,services
- Asistente para publicación web, registro
- Asistente para ordenación de impresión en línea, registro
- register,Web Publishing Wizard
- register,Online Print Ordering Wizard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f5e3f43fe981558fcbf8573eb8768646f112f4816486159cc7c16d71e40e5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608645"
---
# <a name="registering-a-service"></a>Registro de un servicio

Para agregar el servicio a la lista de proveedores en el Asistente para publicación web o en el Asistente para ordenación de impresión en línea, debe agregar la clave adecuada y sus valores al Windows web.

## <a name="required-keys-and-values"></a>Claves y valores necesarios

Para agregar el servicio a la lista de proveedores del Asistente para publicación web, agregue una clave como se muestra a continuación.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Para agregar el servicio a la lista de proveedores del Asistente para ordenación de impresión en línea, agregue una clave como se muestra a continuación.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

Cada uno de los valores es una cadena de tipo REG \_ SZ. Proporcione sus datos como se explica en la tabla siguiente. 

| Nombre del valor     | Explicación                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IconPath       | Ruta de acceso completa al archivo de icono, incluido el nombre de archivo.                                                                                                                                                                                                                                                                                                                                                                        |
| DisplayName    | Nombre que se muestra para el servicio en la lista de proveedores del asistente.                                                                                                                                                                                                                                                                                                                                                             |
| Descripción    | Descripción breve del servicio. Esta descripción también se muestra en la lista de proveedores del asistente directamente debajo del nombre del servicio.                                                                                                                                                                                                                                                                                    |
| Href           | Dirección URL de la primera página del servicio.                                                                                                                                                                                                                                                                                                                                                                                      |
| SupportedTypes | Los tipos de archivo admitidos por el servicio. Por ejemplo, *\*.jpg*. Al especificar solo determinados tipos de archivo, el servicio solo aparece cuando se han seleccionado esos tipos de archivo. Si se ha seleccionado más de un tipo de archivo, el servicio aparece si alguno de esos tipos de archivo es compatible con el servicio. Si desea especificar varios tipos de archivo, separelos en la lista con punto y coma. Por ejemplo, *\*.jpg; \*.bmp*. |



 

A continuación se muestra un ejemplo completo de un servicio de procesamiento de fotos titulado "MyProvider".

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

Cuando se llama a la dirección URL del servicio, se agregan dos valores al final de la dirección URL: lcid y langid. Por ejemplo, la cadena de dirección URL del ejemplo anterior podría ser https: \/ /www.MyProvider.com/Intro.htm?lcid=1033&langid=1033. Estas variables se usan para la información de idioma y localización.

-   **lcid** se usa para informar al servidor de la configuración de país o región e idioma del cliente. No se usa para determinar el idioma de la interfaz de usuario del cliente, sino que se usa para determinar el formato adecuado para la moneda, la fecha y la hora, y otros datos específicos de la región.
-   **langid** se usa para informar al servidor de la configuración de idioma predeterminada del cliente para que pueda usar el idioma adecuado en la interfaz de usuario.

 

 




