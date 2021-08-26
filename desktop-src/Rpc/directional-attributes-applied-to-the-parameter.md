---
title: Atributos direccionales aplicados al parámetro
description: Los atributos direccionales \ in\ y \ out\ determinan cómo el cliente y el servidor asignan y liberan memoria. En la tabla siguiente se resume el efecto de los atributos direccionales en la asignación de memoria.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e18e34a7ea553fd5c1fd9157877a0296e403443fc490bb328f48ac4b7b2c8b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073395"
---
# <a name="directional-attributes-applied-to-the-parameter"></a>Atributos direccionales aplicados al parámetro

Los atributos \[ [direccionales de entrada](/windows/desktop/Midl/in) \] y \[ [salida](/windows/desktop/Midl/out-idl) determinan cómo el cliente \] y el servidor asignan y liberan memoria. En la tabla siguiente se resume el efecto de los atributos direccionales en la asignación de memoria.



| Atributo direccional    | Memoria en el cliente                                                                                            | Memoria en el servidor                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[en](/windows/desktop/Midl/in)\]       | La aplicación cliente debe asignarse antes de la llamada.                                                           | Asignaciones de código auxiliar del servidor.                                                                                                                                  |
| \[[out](/windows/desktop/Midl/out-idl)\] | El código auxiliar de cliente se asigna en la devolución.                                                                            | El código auxiliar del servidor solo asigna puntero de nivel superior; la aplicación de servidor debe asignar todos los punteros incrustados. El servidor también asigna nuevos datos según sea necesario. |
| \[**en**, **out**\]      | La aplicación cliente debe asignar los datos iniciales transmitidos al servidor; el código auxiliar del cliente asigna datos adicionales. | El código auxiliar del servidor asigna los datos iniciales transmitidos desde el cliente; la aplicación de servidor asigna nuevos datos según sea necesario.                                        |



 

En todos estos casos, el código auxiliar del cliente no libera memoria. La aplicación cliente debe liberar la memoria antes de finalizar. El código auxiliar del servidor libera memoria cuando se devuelve la llamada a procedimiento remoto (sujeto al \[ [atributo](/windows/desktop/Midl/allocate) \] ACF asignado).

 

 