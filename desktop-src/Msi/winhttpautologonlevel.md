---
description: La directiva de inicio de sesión automático (inicio de sesión automático) determina cuándo es aceptable que WinHTTP incluya las credenciales predeterminadas en una solicitud al servidor.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: WinHttpAutoLogonLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79fe6c5fe37d44cb74cb0257d3296917905a41a2dc09f84bc13a716a3ee1c1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065745"
---
# <a name="winhttpautologonlevel"></a>WinHttpAutoLogonLevel

La directiva de inicio de sesión automático (inicio de sesión automático) determina cuándo es aceptable que *WinHTTP* incluya las credenciales predeterminadas en una solicitud al servidor.

Puede establecer este valor en **L** para WINHTTP AUTOLOGON SECURITY LEVEL LOW , establecer en **M** para **WINHTTP \_ AUTOLOGON \_ SECURITY LEVEL \_ \_ MEDIUM** y establecer en **H** para **WINHTTP \_ AUTOLOGON \_ SECURITY \_ \_ LEVEL** **\_ \_ \_ \_ HIGH**. El nivel predeterminado es **WINHTTP \_ AUTOLOGON \_ SECURITY LEVEL \_ \_ MEDIUM**. Para más información sobre la directiva de inicio de sesión automático, consulte la sección [Autenticación en WinHTTP.](../winhttp/authentication-in-winhttp.md)

**Windows 8 y Windows Server 2012:** Esta directiva requiere Windows instalador que se ejecuta en Windows 8 o Windows Server 2012 y no está disponible en todas las versiones anteriores de Windows.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ Machine** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ SZ**

 

 
