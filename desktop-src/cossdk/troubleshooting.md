---
description: Solución de problemas
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Solución de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686443"
---
# <a name="troubleshooting"></a>Solución de problemas

Si tiene problemas para diagnosticar los errores de la aplicación, consulte las sugerencias de solución de problemas siguientes:

-   Asegúrese de que el Coordinador de transacciones distribuidas (DTC) se está ejecutando en todos los servidores.
-   Compruebe la comunicación de red comprobando primero en un equipo local para comprobar que la aplicación funciona. Si está ejecutando TCP/IP en la red, puede usar la utilidad de ping.exe para comprobar que los equipos están en la red.
-   Asegúrese de que SQL y DTC están ubicados en el mismo equipo o de que el programa de configuración del cliente de DTC especifica que el DTC está en otro equipo. Si no es así, SQLConnect devolverá un error internamente cuando se llame desde un componente transaccional.
-   Establezca el tiempo de espera de la transacción en un número mayor que el valor predeterminado de 60 segundos. Una vez transcurrido el tiempo de espera de la transacción, COM+ anula la transacción. Todas las llamadas subsiguientes al componente devuelven inmediatamente con el contexto \_ E \_ anulado.
-   Asegúrese de que los controladores ODBC son seguros para subprocesos y no tienen afinidad de subprocesos.
-   Si tiene dificultades para conseguir que una aplicación funcione en varios servidores, reinicie el cliente y, a continuación, compruebe que el controlador de dominio está configurado correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aislamiento de errores y Directiva FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Buscar el origen de un error](finding-the-source-of-an-error.md)
</dt> <dt>

[Cómo modifica COM+ los valores devueltos](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretar códigos de error](interpreting-error-codes.md)
</dt> <dt>

[Estrategias para controlar errores en COM+](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



