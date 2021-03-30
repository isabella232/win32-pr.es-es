---
description: La protección de recursos impide el reemplazo de archivos y carpetas del sistema y las claves del registro esenciales para el sistema operativo. La modificación de los recursos protegidos puede producir un error del sistema o de la aplicación.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Protección de recursos de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361042"
---
# <a name="windows-resource-protection"></a>Protección de recursos de Windows

## <a name="purpose"></a>Propósito

Protección de recursos de Windows (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del registro que se instalan como parte del sistema operativo. Estuvo disponible a partir de Windows Server 2008 y Windows Vista. Las aplicaciones no deben sobrescribir estos recursos porque son utilizados por el sistema y otras aplicaciones. La protección de estos recursos evita errores en la aplicación y en el sistema operativo. WRP es el nuevo nombre de protección de archivos de Windows (WFP). WRP protege las claves del registro y las carpetas, así como los archivos esenciales del sistema.

## <a name="where-applicable"></a>Donde sea aplicable

Todas las aplicaciones basadas en Windows y sus programas de instalación que se ejecutan en Windows Server 2008 o Windows Vista, y en los sistemas operativos posteriores, deben tener en cuenta WRP. Todas las aplicaciones basadas en Windows que se ejecutan en Microsoft Windows Server 2003 o Windows XP y sus programas de instalación deben tener en cuenta WFP.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de WRP está diseñada para que la usen los programadores de C/C++. La API de WRP tiene dos funciones: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) y [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Las aplicaciones que usan solo la función [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) requieren windows Server 2008, Windows Vista, windows Server 2003 o Windows XP. Las aplicaciones que usan la función [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) requieren windows Server 2008 o Windows Vista.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [Acerca de Protección de recursos de Windows](about-windows-file-protection.md)<br/>         | Información general acerca de WRP.<br/>   |
| [Referencia de Protección de recursos de Windows](windows-file-protection-reference.md)<br/> | Documentación de referencia para WRP.<br/> |



 

 

 




