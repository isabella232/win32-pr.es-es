---
description: Información general sobre problemas de confianza parcial y la interfaz de programación de aplicaciones (API) StylusInput.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Consideraciones de confianza parcial para StylusInput API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceda5edfb2e4133bb0fcb3d260ff1e13f9fdb521
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360247"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Consideraciones de confianza parcial para StylusInput API

[**RealTimeStylus**](realtimestylus-class.md) que toma el parámetro *handle* requiere los permisos [UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y [SecurityPermissionFlag.UnmanagedCode,](/previous-versions/windows/) además de los permisos requeridos por el constructor que toma el parámetro *attachedControl.*

Para obtener más información sobre los problemas de seguridad y confianza, vea [Seguridad y confianza.](security-and-trust.md)

 

 
