---
title: Entradas del Registro (COM)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 'Más información sobre: Entradas del Registro (COM)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060889"
---
# <a name="registry-entries-com"></a>Entradas del Registro (COM)

Los valores del Registro de las siguientes claves del Registro controlan aspectos de la funcionalidad de COM:

-   [**Clases HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\**](hkey-local-machine-software-classes.md)
-   [**HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**](hkey-local-machine-software-microsoft-ole.md)
-   [**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion**](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

A partir Windows Server 2003, COM solo usa el token de proceso actual para decidir a qué subárbol del Registro se va a acceder, no el token de subproceso. Si COM no puede acceder al subárbol del Registro de perfiles de usuario, accederá al subárbol **HKEY \_ LOCAL MACHINE \_ \\ System.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
