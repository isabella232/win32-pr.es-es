---
description: Compatibilidad de DEP/NX
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilidad de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b46c9143ee96b8599c10d4c70276d36e20a08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116443"
---
# <a name="depnx-compatibility"></a>Compatibilidad de DEP/NX

De forma predeterminada, en Windows Internet Explorer 7, DEP/NX está deshabilitado por motivos de compatibilidad. Varios complementos populares no son compatibles con DEP/NX y se producirá un error cuando Windows Internet Explorer los cargue con DEP/NX habilitado.

Normalmente, estos complementos se construyen mediante una versión anterior del marco ATL. ATL 7.1 y versiones anteriores no están diseñados con la característica de seguridad DEP. Afortunadamente, las nuevas versiones de Service Pack de Microsoft Windows tienen nuevas API de DEP/NX que le permiten usar DEP/NX y conservar la compatibilidad con versiones anteriores de ATL. Estas nuevas API permiten a Internet Explorer participar en DEP/NX sin provocar un error en los complementos creados mediante versiones anteriores de ATL.

Cuando un complemento no es compatible con DEP/NX y no usa un ATL obsoleto, puede usar una opción de directiva de grupo para no participar en DEP/NX para Internet Explorer hasta que se implemente una versión actualizada del control roto. Los administradores locales pueden controlar DEP/NX ejecutando Internet Explorer como  administrador y desactivando  la opción Habilitar protección de memoria en el panel Opciones **avanzadas de Internet**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
