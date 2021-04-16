---
title: Ver marcas
description: Use las marcas de vista para controlar las vistas de tabla de enrutamiento.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676243"
---
# <a name="view-flags"></a>Ver marcas

Use las marcas de vista para controlar las vistas de tabla de enrutamiento.



| Constante                 | Value      | Descripción                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| \_tamaño máximo de la \_ Dirección RTM \_ | 16         | Tamaño máximo de la dirección de una familia de direcciones.                          |
| \_vistas máximas de RTM \_          | 32         | Número máximo de vistas que pueden estar activas en la tabla de enrutamiento. |
| \_ID. de vista RTM \_ \_ UCAST     | 0          | Especifica una vista de unidifusión.                                        |
| \_ID. de vista RTM \_ \_ MCAST     | 1          | Especifica una vista de multidifusión.                                      |
| tamaño de la \_ máscara de vista RTM \_ \_    | 0x20       | Especifica el número máximo de vistas que se pueden configurar.    |
| vista de RTM de la \_ \_ máscara \_ ninguno    | 0x00000000 | Devuelve información independientemente de la vista.                      |
| RTM \_ Ver \_ máscara \_ cualquiera     | 0x00000000 | Devuelve destinos de todas las vistas. Este es el valor predeterminado.  |
| RTM \_ vista de \_ máscara de \_ UCAST   | 0x00000001 | Devuelve destinos de la vista de unidifusión.                      |
| RTM \_ vista de \_ máscara de \_ MCAST   | 0x00000002 | Devuelve destinos de la vista multidifusión.                    |
| RTM \_ Ver \_ máscara \_ todo     | 0xFFFFFFFF | Devuelve información de todas las vistas.                              |



 

 

 




