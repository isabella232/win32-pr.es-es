---
title: modificador/app_config
description: El \_ modificador/App config selecciona el modo de configuración de la aplicación, que permite usar algunas palabras clave ACF en el archivo IDL. Con este modificador de compilador de MIDL, puede omitir ACF y especificar una interfaz en un solo archivo IDL.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config modificador MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419655"
---
# <a name="app_config-switch"></a>\_modificador de configuración de/App

El modificador **/App \_ config** selecciona el modo de configuración de la aplicación, que permite usar algunas palabras clave ACF en el archivo IDL. Con este modificador de compilador de MIDL, puede omitir ACF y especificar una interfaz en un solo archivo IDL.

``` syntax
midl /app_config
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Microsoft RPC admite el uso de los siguientes atributos ACF en el archivo IDL:

-   \_Identificador implícito
-   \_Identificador automático
-   \_Identificador explícito

Las versiones futuras de Microsoft RPC pueden admitir el uso de otros atributos ACF en el archivo IDL. La opción de **\_ configuración/App** representa una extensión de Microsoft para la especificación de OSF-DCE y, como tal, es mutuamente excluyente con la opción [**/OSF**](-osf.md) .

Para obtener más información relacionada con el modificador **/App \_ config** , vea archivo de configuración de la [aplicación (ACF)](application-configuration-file-acf-.md) y [archivo de definición de interfaz (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Ejemplos

**MIDL/APP \_ config nombreDeArchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




