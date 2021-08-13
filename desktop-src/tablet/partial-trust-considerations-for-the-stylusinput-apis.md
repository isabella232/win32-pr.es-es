---
description: Información general sobre problemas de confianza parcial y la interfaz de programación de aplicaciones (API) StylusInput.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Consideraciones de confianza parcial para StylusInput API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 596e8b50692ae09e9fbaf73f9254afbec8f29d6481a2dc3e27727beb27546441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449355"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Consideraciones de confianza parcial para StylusInput API

[**RealTimeStylus**](realtimestylus-class.md) que toma el parámetro *handle* requiere los permisos [UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) y [SecurityPermissionFlag.UnmanagedCode,](/previous-versions/windows/) además de los permisos requeridos por el constructor que toma el *parámetro attachedControl.*

Para obtener más información sobre los problemas de seguridad y confianza, vea [Seguridad y confianza.](security-and-trust.md)

 

 
