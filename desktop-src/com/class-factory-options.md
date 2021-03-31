---
title: Opciones del generador de clases
description: Opciones del generador de clases
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793972"
---
# <a name="class-factory-options"></a>Opciones del generador de clases

Un control ActiveX, en virtud de ser un objeto COM, debe tener un código de servidor asociado que admita la creación de controles mediante [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) como mínimo.

Es opcional, no es necesario, que este objeto de clase también admite [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) para la administración de licencias. Solo los proveedores que preocupan sobre las licencias deben ser compatibles con el mecanismo de concesión de licencias de COM. En otras palabras, dado que **IClassFactory2** es la única manera de lograr licencias de nivel com, esta interfaz es necesaria en el objeto de clase para los controles que desean tener licencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 