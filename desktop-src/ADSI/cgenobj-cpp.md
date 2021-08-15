---
title: CGENOBJ. Cpp
description: En el componente de proveedor de ejemplo, los métodos Active Directory objeto genéricos, admitidos en cgenobj.cpp, se enumeran en la tabla siguiente.
ms.assetid: 72ccdc6e-1f3e-4633-92b3-500309433337
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0667d44bfb3861989a58ac3764a113b4eb23a87ce3722709a5ca959a0fe4da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962104"
---
# <a name="cgenobjcpp"></a>CGENOBJ. Cpp

En el componente de proveedor de ejemplo, los métodos Active Directory objeto genéricos, admitidos en cgenobj.cpp, se enumeran en la tabla siguiente.



| Método                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObject::CSampleDSGenObject**                                              | Constructor estándar.                                                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::~CSampleDSGenObject**                                             | Destructor estándar.                                                                                                                                                                                                                                                                                                        |
| **CSampleDSGenObject::CreateGenericObject**                                             | Cree un objeto genérico ADS. Inicialice según corresponda.                                                                                                                                                                                                                                                                    |
| **CSampleDSGenObject::SampleDSCreateObject**                                            | Cree este objeto en su contenedor primario.                                                                                                                                                                                                                                                                                 |
| **CSampleDSGenObject::SampleDSSetObject**                                               | Guarde las propiedades de este objeto (borre la memoria caché).                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::AllocateGenObject**                                               | Cree un objeto genérico y cargue sus datos de tipo.                                                                                                                                                                                                                                                                             |
| **CSampleDSGenObject::QueryInterface**                                                  | Devuelve el puntero de interfaz solicitado, si está disponible.                                                                                                                                                                                                                                                                       |
| Métodos [**de IAD estándar,**](/windows/desktop/api/Iads/nn-iads-iads) incluidas las implementaciones para:                   | [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get) (incluida la asignación del tipo de datos nativo al tipo VARIANT) [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) (incluida la asignación del tipo VARIANT al tipo de datos nativo)<br/> [**GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) (actualizar la caché de propiedades)<br/> [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) (guardar la caché de propiedades)<br/> |
| Métodos [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) estándar, incluidas las implementaciones para: | [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)[**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)<br/> [**get \_ Filter**](iadscontainer-property-methods.md)<br/> [**Crear**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)<br/> [**Eliminar**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)<br/>                                            |
| **ConvertSafeArrayToVariantArray**                                                      | Rutina de la utilidad.                                                                                                                                                                                                                                                                                                            |



 

 

 





