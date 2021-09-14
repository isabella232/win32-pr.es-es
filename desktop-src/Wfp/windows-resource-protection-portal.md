---
description: La protección de recursos impide el reemplazo de archivos y carpetas del sistema y claves del Registro esenciales para el sistema operativo. La modificación de recursos protegidos puede provocar errores en la aplicación o en el sistema.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Windows Protección de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249458"
---
# <a name="windows-resource-protection"></a>Windows Protección de recursos

## <a name="purpose"></a>Propósito

Windows Resource Protection (WRP) impide la sustitución de archivos esenciales del sistema, carpetas y claves del Registro que se instalan como parte del sistema operativo. Empezó a estar disponible a partir de Windows Server 2008 y Windows Vista. Las aplicaciones no deben sobrescribir estos recursos porque los usan el sistema y otras aplicaciones. La protección de estos recursos evita errores en la aplicación y el sistema operativo. WRP es el nuevo nombre de Windows File Protection (WFP). WRP protege las claves y carpetas del Registro, así como los archivos esenciales del sistema.

## <a name="where-applicable"></a>Donde sea aplicable

Todas las Windows basadas en Windows y sus programas de instalación que se ejecutan en Windows Server 2008 o Windows Vista, y sistemas operativos posteriores, deben tener en cuenta WRP. Todas Windows basadas en aplicaciones que se ejecutan en Microsoft Windows Server 2003 o Windows XP y sus programas de instalación deben tener en cuenta WFP.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La API de WRP está diseñada para su uso por los programadores de C/C++. La API de WRP tiene dos funciones: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) y [**SfcIsKeyProtected.**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected)

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Las aplicaciones que usan solo la función [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) requieren Windows Server 2008, Windows Vista, Windows Server 2003 o Windows XP. Las aplicaciones que usan [**la función SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) requieren Windows Server 2008 o Windows Vista.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [Acerca de Windows Resource Protection](about-windows-file-protection.md)<br/>         | Información general sobre WRP.<br/>   |
| [Windows Referencia de Resource Protection](windows-file-protection-reference.md)<br/> | Documentación de referencia de WRP.<br/> |



 

 

 




