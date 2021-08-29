---
title: Windows Operaciones de red
description: Una aplicación puede usar las funciones de WNet para examinar, agregar o cancelar conexiones de red en cualquier lugar de la jerarquía de red.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1763f7261dd17fa6f21355ef2f1de404c2b34ec13d6ad6e9769aee3be55283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760345"
---
# <a name="windows-networking-operations"></a>Windows Operaciones de red

Una aplicación puede usar las funciones de WNet para examinar, agregar o cancelar conexiones de red en cualquier lugar de la jerarquía de red.

Una *conexión persistente* es una conexión de red que el sistema restaura automáticamente cuando el usuario inicia sesión. Puede llamar a las funciones [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (o [**WNetAddConnection3)**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)y [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) para controlar si una conexión de red es persistente de una sesión a la siguiente.

Para buscar el nombre de usuario predeterminado o el nombre de usuario usado para establecer una conexión de red, llame a la [**función WNetGetUser.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera)

Además de llamar a las funciones de WNet, un proceso también puede usar mailslots y canalizaciones con nombre para comunicarse con otro proceso. Para obtener más información, [vea Mailslots](/windows/desktop/ipc/mailslots) and [Pipes](/windows/desktop/ipc/pipes).

 

 