---
title: version (atributo)
description: El atributo \ version \ interface identifica una versión determinada entre varias versiones de una interfaz RPC. Con el atributo de versión, se asegura de que solo se permita el enlace de las versiones compatibles del software de cliente y servidor.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- atributo de versión MIDL
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076774"
---
# <a name="version-attribute"></a>version (atributo)

El atributo de interfaz de **\[ versión \]** identifica una versión determinada entre varias versiones de una interfaz RPC. Con el atributo de versión, se asegura de que solo se permita el enlace de las versiones compatibles del software de cliente y servidor.

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor principal* 
</dt> <dd>

Especifica un entero corto sin signo entre cero y 65.535, ambos inclusive, que representa el número de la versión principal.

</dd> <dt>

*valor secundario* 
</dt> <dd>

Especifica un entero corto sin signo entre cero y 65.535, ambos inclusive, que representa el número de versión secundaria. El valor de la versión secundaria es opcional. Si está presente, el valor de la versión secundaria está separado del número de versión principal por un carácter de punto (.). Si no se especifica, el valor de la versión secundaria es cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El compilador MIDL no admite varias versiones de una interfaz COM. Como resultado, una lista de atributos de interfaz que incluye el atributo de **\[** [**objeto**](object.md) **\]** no puede incluir el atributo de **\[ versión \]** . Para crear una nueva versión de una interfaz COM existente, utilice la herencia de interfaz. Una interfaz COM derivada tiene un UUID diferente, pero hereda las funciones miembro de interfaz, los códigos de estado y los atributos de interfaz de la interfaz base.

En combinación con el **\[** valor de [**UUID**](uuid.md) **\]** , el valor de la **\[ \] versión** identifica de forma única la interfaz. La biblioteca en tiempo de ejecución pasa los valores de la **\[ versión \]** y el **\[ UUID \]** al servidor cuando el cliente llama a una función remota. Un cliente puede enlazar con un servidor para una interfaz determinada si:

-   El valor de **\[ UUID \]** es el mismo.
-   El número de versión principal es el mismo.
-   El número de versión secundaria del cliente es menor o igual que el número de versión secundaria del servidor.

Es la ventaja y el beneficio de los usuarios para mantener la compatibilidad ascendente entre versionsÂ, es decir, modificar la interfaz para que solo cambie el número de versión secundaria. Puede conservar la compatibilidad ascendente al agregar nuevos tipos de datos que las funciones existentes no usan y al agregar nuevas funciones sin cambiar la especificación de interfaz para las funciones existentes.

Cambie el número de versión principal si se cumple alguna de las condiciones siguientes:

-   Si cambia un tipo de datos utilizado por una función existente.
-   Si cambia la especificación de interfaz para una función existente (por ejemplo, agregando o quitando un parámetro).
-   Si agrega devoluciones de llamada a las que llaman las funciones existentes.

Cambie el número de versión secundaria si se cumplen todas las condiciones siguientes:

-   Si agrega definiciones de tipo o constantes que no se usan en ninguna función o devoluciones de llamada existentes.
-   Si no cambia ninguna función existente y agrega nuevas funciones a la interfaz.
-   Si agrega devoluciones de llamada a las que no llama ninguna función existente y las nuevas devoluciones de llamada siguen las funciones existentes.

Si las modificaciones se cumplen como un cambio de compatibilidad ascendente de la interfaz, use el procedimiento siguiente.

**Para modificar el archivo de interfaz (IDL)**

1.  Agregue nuevas definiciones de constantes y tipos al archivo de interfaz.
2.  Agregue funciones de devolución de llamada al final del archivo de interfaz.
3.  Agregue nuevas funciones al final del archivo de interfaz.

El atributo **\[ version \]** puede aparecer como máximo una vez en el encabezado de la interfaz.

Cuando el atributo de versión no está presente, la interfaz tiene una versión predeterminada de 0,0.

El carácter de punto entre los números principales y secundarios es un delimitador y no representa un separador decimal. El número secundario se trata como un entero. Los ceros a la izquierda no son significativos. Los ceros a la derecha son significativos.

Por ejemplo, la configuración de versión 1,11 representa un valor principal de uno y un valor menor de once. La versión 1,11 no representa un valor entre 1,1 y 1,2.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[**objeto**](object.md)
</dt> <dt>

[**uuid**](uuid.md)
</dt> </dl>

 

 




