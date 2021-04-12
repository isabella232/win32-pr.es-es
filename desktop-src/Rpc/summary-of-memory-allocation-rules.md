---
title: Resumen de reglas de asignación de memoria
description: En la tabla siguiente se resumen las reglas clave relativas a la asignación de memoria.
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9403bb5057b2004d966c0634bc101a3282fe92
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149457"
---
# <a name="summary-of-memory-allocation-rules"></a>Resumen de reglas de asignación de memoria

En la tabla siguiente se resumen las reglas clave relativas a la asignación de memoria.



| Elemento MIDL                                                                                                                                           | Descripción                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[Punteros [ref](/windows/desktop/Midl/ref) de nivel superior \]                                                                                                                | Debe ser punteros no nulos.                                                                                                                                            |
| Valor devuelto de función                                                                                                                                  | Siempre se asigna una nueva memoria para los valores devueltos del puntero.                                                                                                             |
| \[[Unique](/windows/desktop/Midl/unique), [out](/windows/desktop/Midl/out-idl) \] o \[ [ptr](/windows/desktop/Midl/ptr), puntero de salida \]                                                                   | No permitido por MIDL.                                                                                                                                                  |
| Puntero de no nivel superior \[ [único](/windows/desktop/Midl/unique), [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] o \[ [ptr](/windows/desktop/Midl/ptr), in, out \] que cambia de null a no NULL | Los códigos auxiliares de cliente asignan memoria nueva en el cliente en la devolución.                                                                                                                 |
| Un puntero de un solo nivel no superior \[ [](/windows/desktop/Midl/unique), [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] que cambia de un valor distinto de null a NULL                                 | La memoria está huérfana en el cliente; la aplicación cliente es responsable de liberar memoria y evitar pérdidas.                                                              |
| PTR de nivel superior \[ [](/windows/desktop/Midl/ptr), [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] que cambia de distinto de null a NULL                                       | La memoria quedará huérfana en el cliente si no tiene alias. la aplicación cliente es responsable de liberar y evitar pérdidas de memoria en este caso.                             |
| \[[referencia](/windows/desktop/Midl/ref) \] punteros                                                                                                                           | El nivel de aplicación cliente normalmente asigna.                                                                                                                           |
| No NULL \[ [en](/windows/desktop/Midl/in), puntero de [salida](/windows/desktop/Midl/out-idl) \]                                                                                                | Los códigos auxiliares intentan escribir en el almacenamiento existente en el cliente. Si la **\[ cadena \]** y el tamaño aumentan más allá del tamaño asignado en el cliente, producirá un error de GP en la devolución. |



 

En la tabla siguiente se resumen los efectos de los atributos Key IDL y ACF en la administración de memoria.



| Característica MIDL                                                                   | Problemas del cliente                                                                                                                                  | Problemas del servidor                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[asignar](/windows/desktop/Midl/allocate)( \_ nodo único) \] , \[ asignar (todos los \_ nodos)\]         | Determina si se realizan una o varias llamadas a las funciones de memoria.                                                                         | Lo mismo que el cliente, excepto la memoria privada, a menudo se puede usar para la asignación ( \_ nodo único) \[ en \] y \[ en los datos de salida \] .               |
| \[asignar (gratis) \] o \[ asignar (no \_ gratis)\]                                 | (Ninguno; afecta al servidor).                                                                                                                        | Determina si la memoria del servidor se libera después de cada llamada a procedimiento remoto.                                            |
| los atributos \[ de matriz [Max \_ es](/windows/desktop/Midl/max-is) \] y \[ [size \_ es](/windows/desktop/Midl/size-is)\] | (Ninguno; afecta al servidor).                                                                                                                        | Determina el tamaño de la memoria que se va a asignar.                                                                                    |
| \[[ \_ recuento de bytes](/windows/desktop/Midl/byte-count)\]                                            | El cliente debe asignar el búfer; no asignado o liberado por el código auxiliar del cliente.                                                                           | El atributo del parámetro ACF determina el tamaño del búfer asignado en el servidor.                                                        |
| \[[habilitar \_ asignación](/windows/desktop/Midl/enable-allocate)\]                                  | Normalmente, ninguno. Sin embargo, el cliente puede usar un entorno de administración de memoria diferente.                                                     | El servidor usa un entorno de administración de memoria diferente. [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) debe usarse para las asignaciones. |
| \[[en](/windows/desktop/Midl/in) \] atribui                                                    | Aplicación cliente responsable de la asignación de memoria para los datos.                                                                                 | Asignado en el servidor mediante código auxiliar.                                                                                                 |
| \[[fuera](/windows/desktop/Midl/out-idl) \] de atribui                                             | Asignado en el cliente mediante código auxiliar.                                                                                                                  | \[[fuera](/windows/desktop/Midl/out-idl) \] de -solo el puntero debe ser un puntero de \[ [referencia](/windows/desktop/Midl/ref) \] ; se asigna en el servidor mediante código auxiliar.                       |
| \[[referencia](/windows/desktop/Midl/ref) \] atribui                                                 | La aplicación cliente debe asignar la memoria a la que hace referencia el puntero.                                                                          | Punteros de referencia de nivel superior y de primer nivel administrados por códigos auxiliares.                                                                |
| \[[único](/windows/desktop/Midl/unique) \] atribui                                           | Un valor distinto de null a NULL puede dar lugar a la memoria huérfana; null a un valor distinto de NULL hace que el código auxiliar de cliente llame a la [ \_ \_ asignación de usuarios de MIDL](/windows/desktop/Midl/midl-user-allocate-1). | (Afecta al cliente).                                                                                                             |
| \[[ptr](/windows/desktop/Midl/ptr) \] atribui                                                 | (Consulte \[ [Unique](/windows/desktop/Midl/unique) \] ).                                                                                                              | (Consulte \[ [Unique](/windows/desktop/Midl/unique) \] ).                                                                                             |



 

 

 