---
description: .
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Administración y mantenimiento de imágenes de implementación (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734ac9fae497eeb61d706a228fc1ffc6ea4da264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717056"
---
# <a name="deployment-image-servicing-and-management-dism"></a>Administración y mantenimiento de imágenes de implementación (DISM)

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** de Windows Vista SP1 y versiones posteriores \| Windows 7  
**Servidores** : windows Server 2008 RTM y versiones posteriores \| Windows Server 2008 R2  


## <a name="description"></a>Descripción

La herramienta Administración y mantenimiento de imágenes de implementación (DISM) reemplaza a las herramientas PkgMgr, PEImg y IntlConfg que se están retirando en Windows 7. DISM proporciona una única herramienta centralizada para realizar todas las funciones de estas tres herramientas de una manera más eficaz y estandarizada, eliminando el origen de muchas de las frustraciones que experimentan los usuarios actuales de estas herramientas.

DISM incluye una corrección de compatibilidad para Windows Vista SP1 y versiones posteriores, así como para Windows Server 2008 RTM y versiones posteriores, que redirige las llamadas de PkgMgr desde las aplicaciones heredadas que se ejecutan en Windows 7 a DISM. Si la aplicación se ejecuta en uno de los sistemas operativos compatibles, la corrección de compatibilidad enruta la llamada a PkgMgr. No existe ninguna corrección de compatibilidad para las aplicaciones heredadas que llaman a PEImg o IntlConfg.

## <a name="usage"></a>Uso

DISM es transparente para los usuarios finales de cualquiera de las plataformas admitidas. Sin embargo, si una aplicación llama a PEImg o IntlConfg desde Windows 7, se producirá un error en la llamada.

Actualice los scripts que llaman a PkgMgr, PEImg o IntlConfg para llamar a DISM en su lugar. Es importante incluir la actualización de los scripts de PkgMgr en este esfuerzo, ya que la corrección de compatibilidad que proporciona compatibilidad con versiones anteriores de PkgMgr se quitará en versiones futuras de los sistemas operativos Windows.

Asegúrese de que las llamadas a DISM han reemplazado las llamadas a PkgMgr, PEImg y IntlConfg, y que la operación se ejecuta correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración y mantenimiento de imágenes de implementación (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
