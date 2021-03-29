---
title: Desarrollo de aplicaciones de RPC para Windows
description: Al instalar el kit de desarrollo de software (SDK) de la plataforma, el entorno de desarrollo de RPC siguiente, las bibliotecas en tiempo de ejecución y las herramientas se instalan automáticamente.
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078259"
---
# <a name="developing-rpc-windows-applications"></a>Desarrollo de aplicaciones de RPC para Windows

Al instalar el kit de desarrollo de software (SDK) de la plataforma, se instalan automáticamente el siguiente entorno de desarrollo de RPC, las bibliotecas en tiempo de ejecución y las herramientas:

-   Encabezado del lenguaje C/C++ (. H) archivos
-   Archivos de bibliotecas de importación (. lib) de RPC
-   Programas de ejemplo
-   Archivos de ayuda de referencia de RPC
-   La utilidad **uuidgen**

Al instalar Windows, se instala lo siguiente:

-   Dll en tiempo de ejecución de RPC
-   Microsoft Locator (no se admite en Windows Vista y versiones posteriores)
-   Extremo RPC: servicios de asignación

Las siguientes bibliotecas de importación de RPC.



| Biblioteca de importación | Descripción                |
|----------------|----------------------------|
| Rpcns4. lib     | Funciones de servicio de nombre     |
| Rpcrt4. lib     | Funciones en tiempo de ejecución de Windows |



 

> [!Note]  
> Rpcns4. lib está obsoleto y ya no se admite.

 

Las siguientes bibliotecas de RPC se incluyen para la compatibilidad de nivel inferior.



| Biblioteca de vínculos dinámicos | Descripción                 | Plataforma                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | Transporte de canalización con nombre de cliente | Windows NT, Windows 98 y Windows 95 |
| Rpclts1.dll          | Transporte de canalización con nombre de servidor | Windows NT, Windows 98 y Windows 95 |
| Rpcltc3.dll          | Transporte TCP/IP de cliente     | Windows NT, Windows 98 y Windows 95 |
| Rpclts3.dll          | Transporte TCP/IP del servidor     | Windows NT, Windows 98 y Windows 95 |
| Rpcltc5.dll          | Transporte NetBIOS de cliente    | Windows NT, Windows 98 y Windows 95 |
| Rpclts5.dll          | Transporte NetBIOS de servidor    | Windows NT, Windows 98 y Windows 95 |
| Rpcltc6.dll          | Transporte de cliente SPX        | Windows NT, Windows 98 y Windows 95 |
| Rpclts6.dll          | Transporte de servidor SPX        | Windows NT, Windows 98 y Windows 95 |
| Rpcdgc6.dll          | Transporte IPX de cliente        | Windows NT                         |
| Rpcdgs6.dll          | Transporte de servidor IPX        | Windows NT                         |
| Rpcdgc3.dll          | Transporte UDP de cliente        | Windows NT                         |
| Rpcdgs3.dll          | Transporte UDP de servidor        | Windows NT                         |



 

También necesitará el compilador Lenguaje de definición de interfaz de Microsoft (MIDL). Para obtener más información, vea [usar el compilador de MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).

 

 