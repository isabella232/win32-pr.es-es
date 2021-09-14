---
title: Modificador /app_config
description: El modificador /app config selecciona el modo de configuración de la aplicación, que le permite usar algunas palabras clave \_ de ACF en el archivo IDL. Con este modificador del compilador MIDL, puede omitir el ACF y especificar una interfaz en un único archivo IDL.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config switch MIDL
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159775"
---
# <a name="app_config-switch"></a>Modificador /app \_ config

El **modificador /app \_ config** selecciona el modo de configuración de la aplicación, que le permite usar algunas palabras clave de ACF en el archivo IDL. Con este modificador del compilador MIDL, puede omitir el ACF y especificar una interfaz en un único archivo IDL.

``` syntax
midl /app_config
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Rpc de Microsoft admite el uso de los siguientes atributos de ACF en el archivo IDL:

-   Identificador \_ implícito
-   Identificador \_ automático
-   Identificador \_ explícito

Las versiones futuras de RPC de Microsoft pueden admitir el uso de otros atributos de ACF en el archivo IDL. La **opción /app \_ config** representa una extensión de Microsoft para la especificación OSF-DCE y, como tal, es mutuamente excluyente con la [**opción /osf.**](-osf.md)

Para obtener más información relacionada con el modificador **/app \_ config,** vea Archivo de configuración de [aplicaciones (ACF)](application-configuration-file-acf-.md) y Archivo de definición de [interfaz (IDL).](interface-definition-idl-file.md)

## <a name="examples"></a>Ejemplos

**midl /app \_ config filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




