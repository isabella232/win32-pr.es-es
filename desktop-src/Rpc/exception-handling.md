---
title: Control de excepciones (RPC)
description: RPC utiliza el mismo enfoque para el control de excepciones que la API de Windows.
ms.assetid: 7133d3f4-ed84-4cde-bc77-88e73ced9073
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25de594a648cddb70f26b42e8b0dbf1d6a9dd51d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488843"
---
# <a name="exception-handling-rpc"></a>Control de excepciones (RPC)

RPC utiliza el mismo enfoque para el control de excepciones que la API de Windows.

La estructura RpcEndFinally de RpcFinally de [**RpcTryFinally**](rpctryfinally.md)  /  [](/previous-versions/aa375699(v=vs.80))  /  [](/previous-versions/aa375634(v=vs.80)) es equivalente a la instrucción **try-finally** de Windows. La construcción de excepción RPC [**RpcTryExcept**](rpctryexcept.md)  /  [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  /  [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) es equivalente a la instrucción **try-except de** Windows.

Cuando se usan los controladores de excepciones RPC, el código fuente del lado cliente es portátil. Los diferentes archivos de encabezado RPC proporcionados para cada plataforma resuelven las macros **RpcTry** y [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) para cada plataforma. En el entorno de Windows, estas macros se asignan directamente a las instrucciones **try-finally** y **try-except** de Windows. En otros entornos, estas macros se asignan a otras implementaciones específicas de la plataforma de los controladores de excepciones.

Las posibles excepciones que producen estas estructuras incluyen el conjunto de códigos de error devueltos por las funciones RPC con los prefijos RPC \_ S \_ y RPC \_ X y el conjunto de excepciones que devuelve Windows. Para obtener más información, vea [valores devueltos de RPC](rpc-return-values.md).

Mientras que las macros **RpcTry** y [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) proporcionan una manera personalizable independiente de la plataforma para controlar las excepciones, en Windows Vista y versiones posteriores de Windows, [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) es la forma recomendada de controlar las excepciones. No requiere que se escriban filtros personalizados para capturar muchas de las excepciones estructuradas más comunes. sin embargo, los filtros de excepción personalizados siguen requiriendo **RpcExcept**.

Las excepciones que se producen en la aplicación de servidor, el código auxiliar de servidor y la biblioteca en tiempo de ejecución del servidor (encima del nivel de transporte) se propagan al cliente. Ninguna excepción se propaga desde el nivel de transporte de servidor. El método recomendado para que una rutina de servidor devuelva errores al tiempo de ejecución de RPC es producir una excepción. Una rutina de servidor puede usar cualquier método que sea adecuado para comunicar errores entre las rutinas del servidor, pero si encuentra un error que impide que se ejecute el procedimiento remoto, debe generar una excepción después de la limpieza y antes de volver al tiempo de ejecución de RPC, en lugar de devolver un valor a RPC que solo la rutina de servidor reconoce como un error.

En la siguiente ilustración se muestra cómo se devuelven las excepciones del servidor al cliente.

![las excepciones se devuelven desde el servidor al cliente a través del tiempo de ejecución de RPC respectivo de cada componente](images/prog-a20.png)

Los controladores de excepciones de RPC difieren ligeramente de las macros de control de excepciones Open software Foundation-Distributed Computing Environment (OSF-DCE) **try**, **Finally** y **catch**. Varios proveedores proporcionan archivos de inclusión que asignan las funciones RPC de OSF-DCE a las funciones de Microsoft RPC, entre las que se incluyen **try**, **catch**, **catch** \_ **All** y **ENDTRY**. Estos archivos de encabezado también asignan los códigos de error de RPC \_ s \_ \* en los códigos de error de la excepción de OSF-DCE, los RPC \_ s \_ \* y de asignación \_ de RPC x \_ \* a RPC \_ x \_ \* . Para la portabilidad de OSF-DCE, use estos archivos de inclusión. Para obtener más información sobre los controladores de excepciones RPC, consulte [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter), [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept), [**RpcFinally**](/previous-versions/aa375699(v=vs.80)). Para obtener más información sobre los controladores de excepciones de Windows, vea [control de excepciones estructurado](/windows/desktop/Debug/structured-exception-handling).

 

 
