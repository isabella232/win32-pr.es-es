---
description: Compatibilidad de DEP/NX
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilidad de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65af83e43defb5216b176755dbc8f32067f907620bc120a16aff8b6db3392c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329630"
---
# <a name="depnx-compatibility"></a>Compatibilidad de DEP/NX

De forma predeterminada, en Windows Internet Explorer 7, DEP/NX está deshabilitado por motivos de compatibilidad. Varios complementos populares no son compatibles con DEP/NX y se producirá un error cuando Windows Internet Explorer carga con DEP/NX habilitado.

Normalmente, estos complementos se han creado mediante una versión anterior del marco ATL. ATL 7.1 y versiones anteriores no están diseñados con la característica de seguridad DEP. Afortunadamente, las nuevas versiones de Los Service Pack de Microsoft Windows tienen nuevas API de DEP/NX que le permiten usar DEP/NX y conservar la compatibilidad con versiones anteriores de ATL. Estas nuevas API permiten Internet Explorer participar en DEP/NX sin hacer que se puedan producir errores en los complementos creados mediante versiones anteriores de ATL.

Cuando un complemento no es compatible con DEP/NX y no usa un ATL obsoleto, puede usar una opción de directiva de grupo para rechazar DEP/NX para Internet Explorer hasta que se implemente una versión actualizada del control roto. Los administradores locales pueden controlar DEP/NX ejecutando Internet Explorer como  administrador y desactivando  la opción Habilitar protección de memoria en el panel Opciones avanzadas **de Internet**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
