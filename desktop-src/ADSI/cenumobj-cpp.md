---
title: CENUMOBJ. CPP
description: En el componente de proveedor de ejemplo, la enumeración de un objeto contenedor usa las rutinas, desde cenumobj. cpp, que se enumeran en la tabla siguiente.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b7859571c7136cf1f8a2895b69fe7cdcdf07604
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793797"
---
# <a name="cenumobjcpp"></a>CENUMOBJ. CPP

En el componente de proveedor de ejemplo, la enumeración de un objeto contenedor usa las rutinas, desde cenumobj. cpp, que se enumeran en la tabla siguiente.



| Método                                                 | Descripción                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObjectEnum:: Create**                     | Cree un objeto para habilitar la enumeración de objetos de Active Directory genéricos.                                                                                           |
| **CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**     | Inicialización.                                                                                                                                                       |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Administrar la recuperación de objetos.                                                                                                                                          |
| **CSampleDSGenObjectEnum::FetchObjects**               | Recupera el conjunto de punteros [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que coinciden con el filtro.                                                             |
| **CSampleDSGenObjectEnum::FetchNextObject**            | Recupera un objeto y coincide con el filtro. Si coincide, inclúyalo en el objeto genérico y devuelva un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Administrar la recuperación de los objetos.                                                                                                                                        |
| **CSampleDSGenObjectEnum:: Next**                       | Recupera el número especificado de elementos del objeto de enumeración indicado.                                                                                      |
| **CSampleDSGenObjectEnum::IsValidDSFilter**            | Compruebe que la clase de objeto coincide con una de la lista de filtros.                                                                                                              |
| **CSampleDSGenObjectEnum::BuildDSFilterArray**         | Administrar la matriz de filtros.                                                                                                                                              |
| **CSampleDSGenObjectEnum::CreateAndAppendFilterEntry** | Agregue una nueva clase de objeto al filtro y establezca el filtro como contiguo.                                                                                                |
| **FreeFilterList**                                     | Libere el filtro.                                                                                                                                                      |



 

 

 