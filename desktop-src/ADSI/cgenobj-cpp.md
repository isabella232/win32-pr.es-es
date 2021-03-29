---
title: CGENOBJ. CPP
description: En el componente de proveedor de ejemplo, los métodos de objeto Active Directory genéricos, que se admiten en cgenobj. cpp, se muestran en la tabla siguiente.
ms.assetid: 72ccdc6e-1f3e-4633-92b3-500309433337
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe769dcfa6e4ab607188728115bcba16e40c0e56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773003"
---
# <a name="cgenobjcpp"></a>CGENOBJ. CPP

En el componente de proveedor de ejemplo, los métodos de objeto Active Directory genéricos, que se admiten en cgenobj. cpp, se muestran en la tabla siguiente.



| Método                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObject::CSampleDSGenObject**                                              | Constructor estándar.                                                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject:: ~ CSampleDSGenObject**                                             | Destructor estándar.                                                                                                                                                                                                                                                                                                        |
| **CSampleDSGenObject::CreateGenericObject**                                             | Cree un objeto genérico ADS. Inicialice según corresponda.                                                                                                                                                                                                                                                                    |
| **CSampleDSGenObject::SampleDSCreateObject**                                            | Cree este objeto en su contenedor primario.                                                                                                                                                                                                                                                                                 |
| **CSampleDSGenObject::SampleDSSetObject**                                               | Guarde las propiedades de este objeto (borre la memoria caché).                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::AllocateGenObject**                                               | Cree un objeto genérico y cargue sus datos de tipo.                                                                                                                                                                                                                                                                             |
| **CSampleDSGenObject:: QueryInterface**                                                  | Devuelve el puntero de interfaz solicitado, si está disponible.                                                                                                                                                                                                                                                                       |
| Métodos [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) estándar, incluidas las implementaciones para:                   | [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get) (incluida la asignación del tipo de datos nativo al tipo Variant) [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) (incluida la asignación del tipo Variant al tipo de datos nativo)<br/> [**GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) (actualizar la memoria caché de propiedades)<br/> [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) (guardar la memoria caché de propiedades)<br/> |
| Métodos [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) estándar, incluidas las implementaciones para: | [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)[**Get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)<br/> [**obtener \_ filtro**](iadscontainer-property-methods.md)<br/> [**A**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)<br/> [**Elimínelos**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)<br/>                                            |
| **ConvertSafeArrayToVariantArray**                                                      | Rutina de utilidad.                                                                                                                                                                                                                                                                                                            |



 

 

 





