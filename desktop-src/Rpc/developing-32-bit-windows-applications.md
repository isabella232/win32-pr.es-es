---
title: Desarrollo de aplicaciones de Windows RPC
description: Al instalar el Kit de desarrollo de software de plataforma (SDK), se instalan automáticamente el siguiente entorno de desarrollo RPC, las bibliotecas en tiempo de ejecución y las herramientas.
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ddb48a38faadb8235064fa735fa8a75a80a62308990373ab1971d4a6cd9ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930802"
---
# <a name="developing-rpc-windows-applications"></a>Desarrollo de aplicaciones de Windows RPC

Al instalar el Kit de desarrollo de software de plataforma (SDK), se instalan automáticamente el siguiente entorno de desarrollo RPC, las bibliotecas en tiempo de ejecución y las herramientas:

-   Encabezado del lenguaje C/C++ (. H) archivos
-   Archivos de bibliotecas de importación rpc (.lib)
-   Programas de ejemplo
-   Archivos de Ayuda de referencia rpc
-   La **utilidad uuidgen**

Al instalar Windows, se instala lo siguiente:

-   Archivos DLL en tiempo de ejecución de RPC
-   Localizador de Microsoft (no se admite en Windows Vista y versiones posteriores)
-   Servicios de asignación de puntos de conexión RPC

Las siguientes bibliotecas de importación rpc.



| Importar biblioteca | Descripción                |
|----------------|----------------------------|
| Rpcns4.lib     | Funciones de servicio de nombre     |
| Rpcrt4.lib     | Windows en tiempo de ejecución |



 

> [!Note]  
> Rpcns4.lib está obsoleto y ya no se admite.

 

Las siguientes bibliotecas RPC se incluyen para la compatibilidad de nivel inferior.



| Biblioteca de vínculos dinámicos | Descripción                 | Plataforma                           |
|----------------------|-----------------------------|------------------------------------|
| Rpcltc1.dll          | Transporte de canalización con nombre de cliente | Windows NT, Windows 98, Windows 95 |
| Rpclts1.dll          | Transporte de canalización con nombre del servidor | Windows NT, Windows 98, Windows 95 |
| Rpcltc3.dll          | Transporte TCP/IP de cliente     | Windows NT, Windows 98, Windows 95 |
| Rpclts3.dll          | Transporte TCP/IP del servidor     | Windows NT, Windows 98, Windows 95 |
| Rpcltc5.dll          | Transporte netBIOS de cliente    | Windows NT, Windows 98, Windows 95 |
| Rpclts5.dll          | Transporte NetBIOS del servidor    | Windows NT, Windows 98, Windows 95 |
| Rpcltc6.dll          | Transporte de SPX de cliente        | Windows NT, Windows 98, Windows 95 |
| Rpclts6.dll          | Transporte spx de servidor        | Windows NT, Windows 98, Windows 95 |
| Rpcdgc6.dll          | Transporte IPX de cliente        | Windows NT                         |
| Rpcdgs6.dll          | Transporte IPX del servidor        | Windows NT                         |
| Rpcdgc3.dll          | Transporte UDP de cliente        | Windows NT                         |
| Rpcdgs3.dll          | Transporte UDP del servidor        | Windows NT                         |



 

También necesitará el compilador Lenguaje de definición de interfaz de Microsoft (MIDL). Para obtener más información, [vea Using The MIDL Compiler](/windows/desktop/Midl/using-the-midl-compiler-2).

 

 