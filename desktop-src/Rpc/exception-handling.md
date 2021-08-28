---
title: Control de excepciones (RPC)
description: RPC usa el mismo enfoque para el control de excepciones que Windows API.
ms.assetid: 7133d3f4-ed84-4cde-bc77-88e73ced9073
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b88cea6e1a2046b957baf5afe72be4cbec9f82d7da32215d2434fbf681f64d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080884"
---
# <a name="exception-handling-rpc"></a>Control de excepciones (RPC)

RPC usa el mismo enfoque para el control de excepciones que Windows API.

La [**estructura RpcTryFinally**](rpctryfinally.md)  /  [**RpcFinally**](/previous-versions/aa375699(v=vs.80))  /  [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) es equivalente a Windows **instrucción try-finally.** La construcción de excepción RPC [**RpcTryExcept**](rpctryexcept.md)  /  [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)  /  [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) es equivalente a Windows **instrucción try-except.**

Cuando se usan los controladores de excepciones RPC, el código fuente del lado cliente es portátil. Los diferentes archivos de encabezado RPC proporcionados para cada plataforma resuelven las macros **RpcTry** y [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) para cada plataforma. En el Windows, estas macros se asignan directamente a las instrucciones **try-finally Windows try-finally** y **try-except.** En otros entornos, estas macros se asignan a otras implementaciones específicas de la plataforma de controladores de excepciones.

Las posibles excepciones que estas estructuras han generado incluyen el conjunto de códigos de error devueltos por las funciones RPC con los prefijos RPC S y RPC X y el conjunto de excepciones devuelto \_ \_ por \_ Windows. Para obtener más información, vea [Valores devueltos de RPC.](rpc-return-values.md)

Aunque las macros **RpcTry** y [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) proporcionan una manera personalizable independiente de la plataforma para controlar las excepciones, en Windows Vista y versiones posteriores de Windows, [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) es la manera recomendada de controlar las excepciones. No requiere que se escriban filtros personalizados para capturar muchas de las excepciones estructuradas más comunes. sin embargo, los filtros de excepciones personalizados **todavía requieren RpcExcept**.

Las excepciones que se producen en la aplicación de servidor, el código auxiliar del servidor y la biblioteca en tiempo de ejecución del servidor (por encima de la capa de transporte) se propagan al cliente. No se propaga ninguna excepción desde el nivel de transporte de servidor. El método recomendado para que una rutina de servidor devuelva errores al tiempo de ejecución de RPC es iniciar una excepción. Una rutina de servidor puede usar los métodos adecuados para comunicar errores entre rutinas de servidor, pero si encuentra un error que le impide ejecutar el procedimiento remoto, debe generar una excepción después de limpiar y antes de volver al tiempo de ejecución de RPC, en lugar de devolver un valor a RPC que solo la rutina de servidor reconoce como un error.

En la ilustración siguiente se muestra cómo se devuelven las excepciones del servidor al cliente.

![Las excepciones se devuelven desde el servidor al cliente a través del entorno de ejecución rpc correspondiente de cada componente.](images/prog-a20.png)

Los controladores de excepciones RPC difieren ligeramente de las macros de control de excepciones **TRY**, **FINALLY** y **CATCH** de Open Software Foundation-Distributed Computing Environment (OSF-DCE). Varios proveedores proporcionan archivos de inclusión que asignan las funciones RPC de OSF-DCE a las funciones RPC de Microsoft, **incluidos TRY,** **CATCH,** **CATCH** \_ **ALL** **y ENDTRY.** Estos archivos de encabezado también asignan los códigos de error de RPC S a los homólogos de excepción de \_ \_ \* OSF-DCE, rpc \_ s \_ \* \_ \_ \* \_ \_ \* y asignan códigos de error RPC X a rpc x . Para la portabilidad de OSF-DCE, use estos archivos de incluyen. Para obtener más información sobre los controladores de excepciones RPC, [**vea RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter), [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept), [**RpcFinally**](/previous-versions/aa375699(v=vs.80)). Para obtener más información sobre los controladores Windows excepciones, vea Control estructurado [de excepciones.](/windows/desktop/Debug/structured-exception-handling)

 

 
