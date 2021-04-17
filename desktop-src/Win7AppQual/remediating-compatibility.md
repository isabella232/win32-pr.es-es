---
description: .
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilidad de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb542331d218ed4c493efde091be3e5efae6aee
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717365"
---
# <a name="depnx-compatibility"></a>Compatibilidad de DEP/NX

De forma predeterminada, en Windows Internet Explorer 7, DEP/NX está deshabilitado por motivos de compatibilidad. Varios complementos populares no son compatibles con DEP/NX y producen un error cuando Windows Internet Explorer los carga con DEP/NX habilitado.

Normalmente, estos complementos se compilan con una versión anterior del marco ATL. ATL 7,1 y versiones anteriores no están diseñadas con la característica de seguridad de DEP. Afortunadamente, las nuevas versiones de Microsoft Windows Service Pack tienen nuevas API de DEP/NX que le permiten usar DEP/NX y conservar la compatibilidad con versiones anteriores de ATL. Estas nuevas API permiten que Internet Explorer opte por DEP/NX sin provocar errores en los complementos compilados con versiones anteriores de ATL.

Cuando un complemento no es compatible con DEP/NX y no usa un ATL obsoleto, se puede usar una opción de directiva de grupo para no participar en DEP/NX para Internet Explorer hasta que se implemente una versión actualizada del control roto. Los administradores locales pueden controlar DEP/NX ejecutando Internet Explorer como administrador y desactivando la opción **Habilitar protección de memoria** en el panel **avanzado** de **Opciones de Internet**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
