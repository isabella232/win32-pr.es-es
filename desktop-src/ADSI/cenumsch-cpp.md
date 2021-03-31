---
title: CENUMSCH. CPP
description: En el componente de proveedor de ejemplo, la enumeración de un objeto de esquema usa los métodos, desde cenumsch. cpp, que se enumeran en la tabla siguiente.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcc6d053bb698817ff73db876b00640ed00c8ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903074"
---
# <a name="cenumschcpp"></a>CENUMSCH. CPP

En el componente de proveedor de ejemplo, la enumeración de un objeto de esquema usa los métodos, desde cenumsch. cpp, que se enumeran en la tabla siguiente.



| Método                                        | Descripción                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **CSampleDSSchemaEnum:: Create**               | Cree un objeto para permitir la enumeración de un objeto de clase de esquema ADSI.                                                |
| **CSampleDSSchemaEnum::CSampleDSSchemaEnum**  | Constructor estándar.                                                                                                |
| **CSampleDSSchemaEnum:: ~ CSampleDSSchemaEnum** | Destructor estándar.                                                                                                 |
| **CSampleDSSchemaEnum:: Next**                 | Recupera el número especificado de elementos del objeto de esquema indicado.                                          |
| **CSampleDSSchemaEnum:: EnumObjects**          | Administrar la recuperación de los punteros de interfaz a los objetos del tipo de objeto indicado.                               |
| **CSampleDSSchemaEnum:: EnumObjects**          | Administrar la recuperación de los punteros de interfaz a los objetos del tipo de objeto predeterminado.                                  |
| **CSampleDSSchemaEnum::EnumClasses**          | Administrar la recuperación de punteros de interfaz únicamente a los objetos de clase de esquema incluidos en este objeto.                  |
| **CSampleDSSchemaEnum:: Getclassobject (**       | Recupere la siguiente definición de clase de esquema; Si se encuentra, cree un objeto de clase de esquema y devuelva el puntero de interfaz. |
| **CSampleDSSchemaEnum:: EnumProperties (**       | Administrar la recuperación de los punteros de interfaz a los objetos de propiedad solo contenidos en este objeto.                      |
| **CSampleDSSchemaEnum::GetPropertyObject**    | Recupera la definición de la propiedad siguiente; Si se encuentra, cree un objeto de clase de esquema y devuelva el puntero de interfaz.     |
| **CSampleDSSchemaEnum::EnumSyntaxes**         | Administrar la recuperación de punteros de interfaz a los objetos de sintaxis que solo contiene este objeto.                        |
| **CSampleDSSchemaEnum::GetSyntaxObject**      | Recuperar la siguiente definición de sintaxis; Si se encuentra, cree un objeto de clase de esquema y devuelva el puntero de interfaz.       |



 

 

 




