---
title: CENUMNS. Cpp
description: En el componente de proveedor de ejemplo, la enumeración de un objeto de espacio de nombres usa los métodos, de cenumns.cpp, enumerados en la tabla siguiente.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b86298b27fa097af6ca9607ff2c92dfcdb101a435f9fbd67c60f23467c9e71d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017922"
---
# <a name="cenumnscpp"></a>CENUMNS. Cpp

En el componente de proveedor de ejemplo, la enumeración de un objeto de espacio de nombres usa los métodos, de cenumns.cpp, enumerados en la tabla siguiente.



| Método                                              | Descripción                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSNamespaceEnum::Create**                  | Cree un objeto para permitir la enumeración de un objeto de espacio de nombres ADS.                                                                                         |
| **CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**  | Constructor estándar.                                                                                                                                     |
| **CSampleDSNamespaceEnum::~CSampleDSNamespaceEnum** | Destructor estándar.                                                                                                                                      |
| **CSampleDSNamespaceEnum::Next**                    | Recupere el número especificado de elementos del objeto de espacio de nombres indicado.                                                                            |
| **CSampleDSNamespaceEnum::EnumObjects**             | Administrar la recuperación de los punteros de interfaz a los objetos .                                                                                                  |
| **CSampleDSNamespaceEnum::FetchObjects**            | Capturar el conjunto de [**punteros IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch)                                                                          |
| **CSampleDSNamespaceEnum::FetchNextObject**         | Capturar el objeto siguiente. Si se encuentra, cree un objeto Active Directory y recupere su [**puntero IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) |



 

 

 