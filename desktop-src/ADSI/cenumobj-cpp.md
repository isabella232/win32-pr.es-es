---
title: CENUMOBJ. Cpp
description: En el componente de proveedor de ejemplo, la enumeración de un objeto contenedor usa las rutinas, de cenumobj.cpp, enumeradas en la tabla siguiente.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad1e91a58080dc11f7d8da11f3e3fd59dc2ce75431ee2998d8d4e11011bbb32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023683"
---
# <a name="cenumobjcpp"></a>CENUMOBJ. Cpp

En el componente de proveedor de ejemplo, la enumeración de un objeto contenedor usa las rutinas, de cenumobj.cpp, enumeradas en la tabla siguiente.



| Método                                                 | Descripción                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObjectEnum::Create**                     | Cree un objeto para habilitar la enumeración de objetos Active Directory genéricos.                                                                                           |
| **CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**     | Inicialización.                                                                                                                                                       |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Administrar la recuperación de objetos.                                                                                                                                          |
| **CSampleDSGenObjectEnum::FetchObjects**               | Recupere el conjunto de [**punteros IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que coinciden con el filtro.                                                             |
| **CSampleDSGenObjectEnum::FetchNextObject**            | Recupera un objeto y coincide con el filtro. Si coincide, envolverlo en un objeto genérico y devolver un [**puntero IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Administrar la recuperación de los objetos.                                                                                                                                        |
| **CSampleDSGenObjectEnum::Next**                       | Recupere el número especificado de elementos del objeto de enumeración indicado.                                                                                      |
| **CSampleDSGenObjectEnum::IsValidDSFilter**            | Compruebe que la clase de objeto coincide con una de la lista de filtros.                                                                                                              |
| **CSampleDSGenObjectEnum::BuildDSFilterArray**         | Administrar la matriz de filtros.                                                                                                                                              |
| **CSampleDSGenObjectEnum::CreateAndAppendFilterEntry** | Agregue una nueva clase de objeto al filtro y establezca el filtro como contiguo.                                                                                                |
| **FreeFilterList**                                     | Liberar el filtro.                                                                                                                                                      |



 

 

 