---
title: 'IRootStorage: implementación de archivos compuestos'
description: La implementación de archivos compuestos de COM de IRootStorage permite guardar archivos en situaciones de poca memoria o de poco espacio en disco. Para obtener información sobre cómo se comporta esta interfaz, vea IRootStorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd STG, implementación de archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780106"
---
# <a name="irootstorage---compound-file-implementation"></a>IRootStorage: implementación de archivos compuestos

La implementación de archivos compuestos de COM de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) permite guardar archivos en situaciones de poca memoria o de poco espacio en disco. Para obtener información sobre cómo se comporta esta interfaz, vea **IRootStorage**.

## <a name="when-to-use"></a>Cuándo usar

Use la implementación proporcionada por el sistema de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) solo para admitir el guardado de archivos en condiciones de memoria insuficiente.

## <a name="remarks"></a>Observaciones

Es posible llamar a la implementación de COM de [**IRootStorage:: SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) para realizar una operación de guardar como normal en otro archivo. Sin embargo, las aplicaciones que lo hacen podrían no ser compatibles con las generaciones futuras del almacenamiento COM. Para evitar esta posibilidad, las aplicaciones que realizan una operación de guardar como deben crear manualmente el segundo archivo compuesto e invocar [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto). El método **IRootStorage:: SwitchToFile** solo se debe usar en situaciones de emergencia (memoria insuficiente o espacio en disco).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




