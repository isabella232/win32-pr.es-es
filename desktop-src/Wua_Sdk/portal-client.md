---
description: La API Windows Update Agent (WUA) es un conjunto de interfaces COM que permiten a los administradores y programadores del sistema acceder a Windows Update y Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: Windows Actualización de la API del agente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e7e2c79a707424128082f8f3123cb5fff506a9fc98203ab1fdf8063393310d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738007"
---
# <a name="windows-update-agent-api"></a>Windows Actualización de la API del agente

## <a name="purpose"></a>Propósito

La API Windows Update Agent (WUA) es un conjunto de interfaces COM que permiten a los administradores y programadores del sistema acceder a Windows Update [y Windows Server Update Services (WSUS).](/previous-versions/windows/desktop/ms744624(v=vs.85)) Los scripts y programas se pueden escribir para examinar qué actualizaciones están disponibles actualmente para un equipo y, a continuación, puede instalar o desinstalar actualizaciones.

## <a name="where-applicable"></a>Donde sea aplicable

Los administradores del sistema pueden usar WUA para determinar mediante programación qué actualizaciones se deben aplicar a un equipo, descargar esas actualizaciones y, a continuación, instalarlas con poca o ninguna intervención del usuario.

Los proveedores de software independientes (ISV) y los desarrolladores de usuarios finales pueden integrar las características de WUA en la administración de equipos o en el software de administración de actualizaciones para proporcionar un entorno operativo sin problemas.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Puede escribir aplicaciones WUA en varios lenguajes de programación. WUA define interfaces y objetos a los que se puede acceder desde Visual Basic, Visual Basic Scripting Edition (VBScript), JScript y desde C y C++. La familiaridad con la programación COM es útil para el programador de WUA.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

WUA se admite a partir de Windows XP. WUA se admite en el servidor a partir de Windows Server 2003.

## <a name="in-this-section"></a>En esta sección

-   [Uso de la API Windows Update Agent](using-the-windows-update-agent-api.md)
-   [Referencia de LA API de WUA](windows-update-agent--wua--api-reference.md)

 

 
