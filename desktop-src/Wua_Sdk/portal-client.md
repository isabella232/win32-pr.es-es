---
description: La API del agente de Windows Update (WUA) es un conjunto de interfaces COM que permiten a los programadores y desarrolladores del sistema tener acceso a Windows Update y Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: API del agente Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808648"
---
# <a name="windows-update-agent-api"></a>API del agente Windows Update

## <a name="purpose"></a>Propósito

La API del agente de Windows Update (WUA) es un conjunto de interfaces COM que permiten a los programadores y desarrolladores del sistema tener acceso a Windows Update y [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)). Se pueden escribir scripts y programas para examinar las actualizaciones que están disponibles actualmente para un equipo y, a continuación, puede instalar o desinstalar las actualizaciones.

## <a name="where-applicable"></a>Donde sea aplicable

Los administradores del sistema pueden usar WUA para determinar mediante programación qué actualizaciones se deben aplicar a un equipo, descargar dichas actualizaciones y, a continuación, instalarlas con poca o ninguna intervención del usuario.

Los fabricantes de software independientes (ISV) y los desarrolladores de usuarios finales pueden integrar las características de WUA en el software de administración de equipos o de administración de actualizaciones para proporcionar un entorno operativo sin problemas.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Puede escribir aplicaciones de WUA en varios lenguajes de programación. WUA define interfaces y objetos a los que se puede tener acceso desde Visual Basic, Visual Basic Scripting Edition (VBScript), JScript y desde C y C++. Una familiaridad con la programación COM es útil para el programador de WUA.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

WUA se admite a partir de Windows XP. WUA se admite en el servidor a partir de Windows Server 2003.

## <a name="in-this-section"></a>En esta sección

-   [Uso de la API del agente Windows Update](using-the-windows-update-agent-api.md)
-   [Referencia de la API de WUA](windows-update-agent--wua--api-reference.md)

 

 
