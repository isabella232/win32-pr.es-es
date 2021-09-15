---
title: Opciones del generador de clases
description: Opciones del generador de clases
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574105"
---
# <a name="class-factory-options"></a>Opciones del generador de clases

Un ActiveX control, en virtud de ser un objeto COM, debe tener código de servidor asociado que admita la creación de controles a través de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) como mínimo.

Es opcional, no necesario, que este objeto de clase también admita [**IClassFactory2 para**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) la administración de licencias. Solo los proveedores a los que les preocupa la concesión de licencias deben admitir el mecanismo de licencias de COM. En otras palabras, dado que **IClassFactory2** es la única manera de lograr licencias de nivel COM, esta interfaz es necesaria en el objeto de clase para los controles que desean tener licencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 