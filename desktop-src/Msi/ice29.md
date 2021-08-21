---
description: ICE29 valida que los nombres de flujo truncados sigan siendo únicos. Se valida cualquier tabla que tenga una columna Binary u Object. Consulte el tipo de datos de la columna Binary.
ms.assetid: a51b641d-992b-4b6b-a208-d94bc7d05115
title: ICE29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdef203e314a087e9eb11bcf1b958425d7608028d979db925edce1b42e4bebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528715"
---
# <a name="ice29"></a>ICE29

ICE29 valida que los nombres de flujo truncados sigan siendo únicos. Se valida cualquier tabla que tenga una columna Binary u Object. Consulte el [tipo de datos de](binary.md) la columna Binary.

El control de secuencias mediante la implementación de almacenamiento estructurado OLE de Win32 limita los nombres de secuencia. Vea [Limitaciones de OLE Secuencias](ole-limitations-on-streams.md). El instalador puede comprimir nombres de secuencia de hasta 62 caracteres de longitud. Los nombres más largos que este se truncan.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



