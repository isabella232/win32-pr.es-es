---
description: La protección de recursos evita el reemplazo de archivos y carpetas del sistema y claves del Registro esenciales para el sistema operativo. La modificación de recursos protegidos puede provocar errores en la aplicación o en el sistema.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Windows Protección de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00dabeadc662d3c13923d9d56e442388c53b7fa1e5740c651d689c3098bd049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098585"
---
# <a name="windows-resource-protection"></a>Windows Protección de recursos

## <a name="purpose"></a>Propósito

Windows Protección de recursos (WRP) impide el reemplazo de archivos esenciales del sistema, carpetas y claves del Registro que se instalan como parte del sistema operativo. Estaba disponible a partir de Windows Server 2008 y Windows Vista. Las aplicaciones no deben sobrescribir estos recursos porque los usan el sistema y otras aplicaciones. La protección de estos recursos evita errores en la aplicación y el sistema operativo. WRP es el nuevo nombre de Windows File Protection (WFP). WRP protege las claves y carpetas del Registro, así como los archivos esenciales del sistema.

## <a name="where-applicable"></a>Donde sea aplicable

Todas las Windows basadas en Windows y sus programas de instalación que se ejecutan en Windows Server 2008 o Windows Vista y sistemas operativos posteriores deben tener en cuenta WRP. Todas Windows basadas en aplicaciones que se ejecutan en Microsoft Windows Server 2003 o Windows XP y sus programas de instalación deben tener en cuenta WFP.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de WRP está diseñada para que la usen los programadores de C/C++. La API de WRP tiene dos funciones: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) y [**SfcIsKeyProtected.**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected)

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Las aplicaciones que solo usan la función [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) requieren Windows Server 2008, Windows Vista, Windows Server 2003 o Windows XP. Las aplicaciones que usan [**la función SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) requieren Windows Server 2008 o Windows Vista.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [Acerca de Windows Resource Protection](about-windows-file-protection.md)<br/>         | Información general sobre WRP.<br/>   |
| [Windows Referencia de Resource Protection](windows-file-protection-reference.md)<br/> | Documentación de referencia de WRP.<br/> |



 

 

 




