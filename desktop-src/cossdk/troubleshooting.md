---
description: Solución de problemas
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Solución de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e10877306dc17f0b04718037a4bc073c8a7ed7c7c4ac46b31cda90517d22b7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118812011"
---
# <a name="troubleshooting"></a>Solución de problemas

Si tiene problemas para diagnosticar los errores de la aplicación, consulte las siguientes sugerencias de solución de problemas:

-   Asegúrese de que el Coordinador de transacciones distribuidas (DTC) se ejecuta en todos los servidores.
-   Compruebe la comunicación de red probando primero en un equipo local para comprobar que la aplicación funciona. Si ejecuta TCP/IP en la red, puede usar la utilidad ping.exe para comprobar que las máquinas están en la red.
-   Asegúrese de que SQL Y DTC se encuentran en el mismo equipo o que el programa de configuración de cliente de DTC especifica que el DTC está en otro equipo. Si no es así, SQLConnect devolverá un error internamente cuando se llame desde un componente transaccional.
-   Establezca el tiempo de espera de la transacción en un número mayor que el valor predeterminado de 60 segundos. Una vez transcurrido el tiempo de espera de la transacción, COM+ anula la transacción. Todas las llamadas posteriores al componente se devuelven inmediatamente con CONTEXT \_ E \_ ABORTED.
-   Asegúrese de que los controladores ODBC son seguros para subprocesos y no tienen afinidad de subproceso.
-   Si tiene dificultades para que una aplicación funcione en varios servidores, reinicie el cliente y compruebe que el controlador de dominio está configurado correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aislamiento de errores y directiva de error](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Buscar el origen de un error](finding-the-source-of-an-error.md)
</dt> <dt>

[Cómo com+ modifica los valores devueltos](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretación de códigos de error](interpreting-error-codes.md)
</dt> <dt>

[Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



