---
title: Opciones de generador de clases
description: Opciones de generador de clases
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 720016aa42057047fa0980c1219dd4fe787198fea4c0ccc7d7f86d45a634a672
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859585"
---
# <a name="class-factory-options"></a>Opciones de generador de clases

Un ActiveX control, en virtud de ser un objeto COM, debe tener código de servidor asociado que admita la creación de controles a través de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) como mínimo.

Es opcional, no necesario, que este objeto de clase también admita [**IClassFactory2 para**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) la administración de licencias. Solo los proveedores que estén interesados en las licencias deben admitir el mecanismo de licencias de COM. En otras palabras, dado que **IClassFactory2** es la única manera de lograr licencias de nivel COM, esta interfaz es necesaria en el objeto de clase para los controles que desean tener licencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 