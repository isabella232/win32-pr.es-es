---
title: CPRPOBJ. Cpp
description: En el componente de proveedor de ejemplo, los métodos de objeto de propiedad, en cprpobj.cpp, se enumeran en la tabla siguiente.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb130d6deced939aa718e839c0e7f178329e6a5b14c383dbf1a2719c0f25cfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840339"
---
# <a name="cprpobjcpp"></a>CPRPOBJ. Cpp

En el componente de proveedor de ejemplo, los métodos de objeto de propiedad, en cprpobj.cpp, se enumeran en la tabla siguiente.



| Método                                                 | Descripción                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSProperty::CSampleDSProperty**               | Constructor estándar.                                                                                                                          |
| **CSampleDSProperty::~CSampleDSProperty**              | Destructor estándar.                                                                                                                           |
| **CSampleDSProperty::CreateProperty**                  | Cree un objeto ADS Property y busque las definiciones de atributo mediante una llamada **a SampleDSGetPropertyDefinition**.                              |
| **CSampleDSProperty::CreateProperty**                  | Dada la definición de atributo, cree un objeto de propiedad, estableciendo la correspondencia entre las sintaxis de ADS admitidas y las sintaxis del proveedor. |
| **CSampleDSProperty::AllocatePropertyObject**          | Cree un objeto de propiedad y cargue sus datos de tipo.                                                                                               |
| **CSampleDSProperty::QueryInterface**                  | Devuelve el puntero de interfaz solicitado, si está disponible.                                                                                          |
| Métodos [**de los IAD estándar.**](/windows/desktop/api/Iads/nn-iads-iads)                 |                                                                                                                                                |
| Métodos [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) estándar. |                                                                                                                                                |
| **MapSyntaxIdtoADsSyntax**                             | Establezca la correspondencia entre el identificador de sintaxis y la sintaxis ads.                                                                               |
| **MapSyntaxIdtoSampleDSSyntax**                        | Establezca la correspondencia entre el identificador de sintaxis y la sintaxis del proveedor.                                                                          |



 

 

 




