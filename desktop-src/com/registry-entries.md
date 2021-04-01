---
title: Entradas del registro (COM)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 'Más información acerca de: entradas del registro (COM)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153472"
---
# <a name="registry-entries-com"></a>Entradas del registro (COM)

Los valores del registro en las siguientes claves del registro controlan aspectos de la funcionalidad de COM:

-   [**HKEY \_ \_ clases de \\ software de máquina local \\**](hkey-local-machine-software-classes.md)
-   [**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**](hkey-local-machine-software-microsoft-ole.md)
-   [**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

A partir de Windows Server 2003, COM usa solo el token de proceso actual para decidir a qué subárbol del registro acceder, no el token de subproceso. Si COM no puede tener acceso al subárbol del registro del perfil de usuario, tendrá acceso al subárbol del **\_ \_ \\ sistema del equipo local HKEY** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
