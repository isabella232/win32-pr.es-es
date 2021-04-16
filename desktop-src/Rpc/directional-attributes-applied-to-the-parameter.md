---
title: Atributos direccionales aplicados al parámetro
description: Los atributos direccionales \ in \ y \ out \ determinan el modo en que el cliente y el servidor asignan y liberan memoria. En la tabla siguiente se resume el efecto de los atributos direccionales en la asignación de memoria.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676457"
---
# <a name="directional-attributes-applied-to-the-parameter"></a>Atributos direccionales aplicados al parámetro

Los atributos direccionales \[ [dentro](/windows/desktop/Midl/in) \] y \[ [fuera](/windows/desktop/Midl/out-idl) \] determinan cómo el cliente y el servidor asignan y liberan memoria. En la tabla siguiente se resume el efecto de los atributos direccionales en la asignación de memoria.



| Atributo direccional    | Memoria en el cliente                                                                                            | Memoria en el servidor                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[en](/windows/desktop/Midl/in)\]       | La aplicación cliente debe asignarse antes de la llamada.                                                           | El código auxiliar del servidor asigna.                                                                                                                                  |
| \[[fuera](/windows/desktop/Midl/out-idl) de\] | El código auxiliar del cliente se asigna en la devolución.                                                                            | El código auxiliar del servidor asigna solo el puntero de nivel superior; la aplicación de servidor debe asignar todos los punteros incrustados. El servidor también asigna nuevos datos según sea necesario. |
| \[**in**, **out**\]      | La aplicación cliente debe asignar los datos iniciales transmitidos al servidor; el código auxiliar de cliente asigna datos adicionales. | El código auxiliar del servidor asigna los datos iniciales transmitidos desde el cliente; la aplicación de servidor asigna nuevos datos según sea necesario.                                        |



 

En todos estos casos, el código auxiliar de cliente no libera memoria. La aplicación cliente debe liberar la memoria antes de que finalice. El código auxiliar del servidor libera memoria cuando la llamada a procedimiento remoto devuelve (sujeto al \[ atributo [asignar](/windows/desktop/Midl/allocate) \] ACF).

 

 