---
title: CENUMNS. CPP
description: En el componente de proveedor de ejemplo, la enumeración de un objeto de espacio de nombres usa los métodos, desde cenumns. cpp, que se enumeran en la tabla siguiente.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656391"
---
# <a name="cenumnscpp"></a>CENUMNS. CPP

En el componente de proveedor de ejemplo, la enumeración de un objeto de espacio de nombres usa los métodos, desde cenumns. cpp, que se enumeran en la tabla siguiente.



| Método                                              | Descripción                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSNamespaceEnum:: Create**                  | Cree un objeto para permitir la enumeración de un objeto de espacio de nombres ADS.                                                                                         |
| **CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**  | Constructor estándar.                                                                                                                                     |
| **CSampleDSNamespaceEnum:: ~ CSampleDSNamespaceEnum** | Destructor estándar.                                                                                                                                      |
| **CSampleDSNamespaceEnum:: Next**                    | Recupera el número especificado de elementos del objeto de espacio de nombres indicado.                                                                            |
| **CSampleDSNamespaceEnum:: EnumObjects**             | Administrar la recuperación de punteros de interfaz a los objetos.                                                                                                  |
| **CSampleDSNamespaceEnum::FetchObjects**            | Recupera el conjunto de punteros [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .                                                                          |
| **CSampleDSNamespaceEnum::FetchNextObject**         | Captura el siguiente objeto. Si se encuentra, cree un objeto de Active Directory genérico y recupere su puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . |



 

 

 