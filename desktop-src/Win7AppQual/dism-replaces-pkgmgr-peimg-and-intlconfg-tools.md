---
description: Administración y mantenimiento de imágenes de implementación (DISM)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Administración y mantenimiento de imágenes de implementación (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d16233927dca2d5dba296fd33fb64135f691e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088493"
---
# <a name="deployment-image-servicing-and-management-dism"></a>Administración y mantenimiento de imágenes de implementación (DISM)

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows Vista SP1 y \| versiones posteriores de Windows 7  
**Servidores:** Windows Server 2008 RTM y \| versiones posteriores de Windows Server 2008 R2  


## <a name="description"></a>Descripción

La herramienta Administración y mantenimiento de imágenes de implementación (DISM) reemplaza las herramientas pkgmgr, PEImg e IntlConfg que se van a retirar en Windows 7. DISM proporciona una única herramienta centralizada para realizar todas las funciones de estas tres herramientas de una manera más eficaz y estandarizada, lo que elimina el origen de muchas de las frustraciones que experimentan los usuarios actuales de estas herramientas.

DISM incluye una corrección de compatibilidad (shim) para Windows Vista SP1 y versiones posteriores, así como para Windows Server 2008 RTM y versiones posteriores, que redirige las llamadas de pkgmgr desde aplicaciones heredadas que se ejecutan en Windows 7 a DISM. Si la aplicación se ejecuta en uno de los sistemas operativos compatibles, la corrección de compatibilidad (shim) enruta la llamada a pkgmgr. No existen correcciones de compatibilidad (shim) para las aplicaciones heredadas que llaman a PEImg o IntlConfg.

## <a name="usage"></a>Uso

DISM es transparente para los usuarios finales de pkgmgr en cualquiera de las plataformas admitidas. Sin embargo, si una aplicación llama a PEImg o IntlConfg desde Windows 7, se producirá un error en la llamada.

Actualice los scripts que llaman a pkgmgr, PEImg o IntlConfg para llamar a DISM en su lugar. Es importante incluir la actualización de scripts de pkgmgr en este esfuerzo, ya que la corrección de compatibilidad con versiones anteriores de pkgmgr se quitará en versiones futuras de los sistemas operativos Windows.

Asegúrese de que las llamadas a DISM han reemplazado las llamadas a pkgmgr, PEImg e IntlConfg, y que la operación se ejecuta correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración y mantenimiento de imágenes de implementación (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
