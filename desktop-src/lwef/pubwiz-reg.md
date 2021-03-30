---
title: Registrar un servicio
description: Para agregar el servicio a la lista de proveedores en el Asistente para publicación web o en el Asistente para la ordenación de impresión en línea, debe agregar la clave adecuada y sus valores al registro de Windows.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- registro, servicios
- Asistente para publicación Web, registrar
- Asistente para pedir copias fotográficas en línea, registrar
- registro, Asistente para publicación Web
- registro, Asistente para orden de impresión en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104280213"
---
# <a name="registering-a-service"></a>Registrar un servicio

Para agregar el servicio a la lista de proveedores en el Asistente para publicación web o en el Asistente para la ordenación de impresión en línea, debe agregar la clave adecuada y sus valores al registro de Windows.

## <a name="required-keys-and-values"></a>Claves y valores necesarios

Para agregar el servicio a la lista de proveedores para el Asistente para publicación Web, agregue una clave tal como se muestra a continuación.

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

Para agregar el servicio a la lista de proveedores para el Asistente para la ordenación de impresión en línea, agregue una clave tal como se muestra a continuación.

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

Cada uno de los valores es una cadena de tipo REG \_ SZ. Proporcione sus datos tal y como se explica en la tabla siguiente. 

| Nombre del valor     | Explicación                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IconPath       | Ruta de acceso completa al archivo de icono, incluido el nombre de archivo.                                                                                                                                                                                                                                                                                                                                                                        |
| DisplayName    | El nombre que se muestra para el servicio en la lista de proveedores del asistente.                                                                                                                                                                                                                                                                                                                                                             |
| Descripción    | Breve descripción del servicio. Esta descripción también se muestra en la lista de proveedores del asistente, justo debajo del nombre del servicio.                                                                                                                                                                                                                                                                                    |
| REFERENCIA           | La dirección URL de la primera página de su servicio.                                                                                                                                                                                                                                                                                                                                                                                      |
| SupportedTypes | Los tipos de archivo admitidos por el servicio. Por ejemplo, *\* . jpg*. Al especificar solo determinados tipos de archivo, el servicio solo aparece cuando se han seleccionado esos tipos de archivo. Si se ha seleccionado más de un tipo de archivo, el servicio aparece si el servicio admite cualquiera de estos tipos de archivo. Si desea especificar varios tipos de archivo, sepárelos en la lista con punto y coma. Por ejemplo, *\* . jpg; \* . BMP*. |



 

A continuación se incluye un ejemplo completo de un servicio de procesamiento de fotografías titulado "nodataprovider".

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

Cuando se llama a la dirección URL de su servicio, se agregan dos valores al final de la dirección URL: LCID y langid. Por ejemplo, la cadena de dirección URL para el ejemplo anterior podría ser https: \/ /www.MyProvider.com/Intro.htm? LCID = 1033&langid = 1033. Estas variables se usan para la información de idioma y localización.

-   **LCID** se usa para informar al servidor de la configuración de idioma y país o región del cliente. No se utiliza para determinar el idioma de la interfaz de usuario del cliente, sino que se usa para determinar el formato correcto de moneda, fecha y hora y otros datos específicos de la región.
-   **langid** se usa para informar al servidor de la configuración de idioma predeterminado del cliente para que pueda usar el idioma adecuado en la interfaz de usuario.

 

 




