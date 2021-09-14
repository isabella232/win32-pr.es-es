---
description: La directiva de inicio de sesión automático (inicio de sesión automático) determina cuándo es aceptable que WinHTTP incluya las credenciales predeterminadas en una solicitud al servidor.
ms.assetid: 4ED8B6BC-E52D-4DE9-A9AE-1FDF61A978A9
title: WinHttpAutoLogonLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7760faa94e24b7fe5b33717c504b03e4de42c0aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253976"
---
# <a name="winhttpautologonlevel"></a>WinHttpAutoLogonLevel

La directiva de inicio de sesión automático (inicio de sesión automático) determina cuándo es aceptable que *WinHTTP* incluya las credenciales predeterminadas en una solicitud al servidor.

Puede establecer este valor en **L** para WINHTTP AUTOLOGON SECURITY LEVEL LOW , establecer en **M** para **WINHTTP \_ AUTOLOGON \_ SECURITY LEVEL \_ \_ MEDIUM** y establecer en **H** para **WINHTTP \_ AUTOLOGON \_ SECURITY \_ \_ LEVEL** **\_ \_ \_ \_ HIGH**. El nivel predeterminado es **WINHTTP \_ AUTOLOGON \_ SECURITY LEVEL \_ \_ MEDIUM**. Para más información sobre la directiva de inicio de sesión automático, consulte la sección [Autenticación en WinHTTP.](../winhttp/authentication-in-winhttp.md)

**Windows 8 y Windows Server 2012:** Esta directiva requiere Windows instalador que se ejecuta en Windows 8 o Windows Server 2012 y no está disponible en todas las versiones anteriores de Windows.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ SZ**

 

 
