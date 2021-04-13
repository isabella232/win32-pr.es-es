---
title: CPRPOBJ. CPP
description: En el componente proveedor de ejemplo, los métodos de objeto de propiedad, en cprpobj. cpp, se muestran en la tabla siguiente.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268264"
---
# <a name="cprpobjcpp"></a>CPRPOBJ. CPP

En el componente proveedor de ejemplo, los métodos de objeto de propiedad, en cprpobj. cpp, se muestran en la tabla siguiente.



| Método                                                 | Descripción                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSProperty::CSampleDSProperty**               | Constructor estándar.                                                                                                                          |
| **CSampleDSProperty:: ~ CSampleDSProperty**              | Destructor estándar.                                                                                                                           |
| **CSampleDSProperty:: CreateProperty**                  | Cree un objeto de propiedad ADS, buscando las definiciones de atributo mediante una llamada a **SampleDSGetPropertyDefinition**.                              |
| **CSampleDSProperty:: CreateProperty**                  | Dada la definición de atributo, cree un objeto de propiedad y establezca la correspondencia entre las sintaxis de ADS admitidas y las sintaxis del proveedor. |
| **CSampleDSProperty::AllocatePropertyObject**          | Cree un objeto de propiedad y cargue sus datos de tipo.                                                                                               |
| **CSampleDSProperty:: QueryInterface**                  | Devuelve el puntero de interfaz solicitado, si está disponible.                                                                                          |
| Métodos [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) estándar.                 |                                                                                                                                                |
| Métodos estándar de [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) . |                                                                                                                                                |
| **MapSyntaxIdtoADsSyntax**                             | Establezca la correspondencia entre el identificador de sintaxis y la sintaxis de ADS.                                                                               |
| **MapSyntaxIdtoSampleDSSyntax**                        | Establezca la correspondencia entre el identificador de sintaxis y la sintaxis del proveedor.                                                                          |



 

 

 




