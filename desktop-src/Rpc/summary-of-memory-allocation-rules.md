---
title: Resumen de las reglas de asignación de memoria
description: En la tabla siguiente se resumen las reglas clave relativas a la asignación de memoria.
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec50632693ad0df7ff44aa1d2a9a2760b07a2ed1b72a13ac5dc33294569c3484
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924706"
---
# <a name="summary-of-memory-allocation-rules"></a>Resumen de las reglas de asignación de memoria

En la tabla siguiente se resumen las reglas clave relativas a la asignación de memoria.



| Elemento MIDL                                                                                                                                           | Descripción                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Punteros \[ [ref de nivel](/windows/desktop/Midl/ref) \] superior                                                                                                                | Deben ser punteros que no sean NULL.                                                                                                                                            |
| Valor devuelto de función                                                                                                                                  | Siempre se asigna nueva memoria para los valores devueltos del puntero.                                                                                                             |
| \[[unique](/windows/desktop/Midl/unique), [out](/windows/desktop/Midl/out-idl) \] o \[ [ptr](/windows/desktop/Midl/ptr), puntero \] out                                                                   | MIDL no permite.                                                                                                                                                  |
| Puntero único que no es \[ [de nivel](/windows/desktop/Midl/unique)superior, [en](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] o \[ [ptr](/windows/desktop/Midl/ptr), en, puntero out que cambia de \] null a non-null | Los códigos auxiliares de cliente asignan nueva memoria en el cliente a la devolución.                                                                                                                 |
| Único de nivel \[ [superior,](/windows/desktop/Midl/unique) [en](/windows/desktop/Midl/in), [puntero de](/windows/desktop/Midl/out-idl) salida que cambia de \] no NULL a NULL                                 | La memoria está huérfana en el cliente; la aplicación cliente es responsable de liberar memoria y evitar pérdidas.                                                              |
| ptr de nivel no \[ [superior](/windows/desktop/Midl/ptr), [en](/windows/desktop/Midl/in), [puntero de](/windows/desktop/Midl/out-idl) salida que cambia de \] no NULL a NULL                                       | La memoria estará huérfana en el cliente si no tiene alias; la aplicación cliente es responsable de liberar y evitar pérdidas de memoria en este caso.                             |
| \[[ref](/windows/desktop/Midl/ref) \] Punteros                                                                                                                           | El nivel de aplicación de cliente normalmente asigna.                                                                                                                           |
| Puntero distinto de NULL \[ [en](/windows/desktop/Midl/in), [](/windows/desktop/Midl/out-idl) \] out                                                                                                | Los códigos auxiliares intentan escribir en el almacenamiento existente en el cliente. Si **\[ la cadena \]** y el tamaño aumentan más allá del tamaño asignado en el cliente, provocará un error de GP en la devolución. |



 

En la tabla siguiente se resumen los efectos de los atributos clave IDL y ACF en la administración de memoria.



| Característica MIDL                                                                   | Problemas del cliente                                                                                                                                  | Problemas del servidor                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[allocate](/windows/desktop/Midl/allocate)(nodo \_ único) \] , \[ allocate(all \_ nodes)\]         | Determina si se realizan una o varias llamadas a las funciones de memoria.                                                                         | Igual que el cliente, excepto la memoria privada, a menudo se puede usar para asignar (nodo único) en los datos de entrada \_ \[ y \] \[ \] salida.               |
| \[allocate(free) \] o \[ allocate(don't \_ free)\]                                 | (Ninguno; afecta al servidor).                                                                                                                        | Determina si la memoria del servidor se libera después de cada llamada a procedimiento remoto.                                            |
| el valor \[ [máximo de los atributos de \_ la matriz](/windows/desktop/Midl/max-is) \] es y el tamaño \[ [ \_ es](/windows/desktop/Midl/size-is)\] | (Ninguno; afecta al servidor).                                                                                                                        | Determina el tamaño de memoria que se va a asignar.                                                                                    |
| \[[recuento de \_ bytes](/windows/desktop/Midl/byte-count)\]                                            | El cliente debe asignar el búfer; no se asignan ni liberan mediante códigos auxiliares de cliente.                                                                           | El atributo de parámetro ACF determina el tamaño del búfer asignado en el servidor.                                                        |
| \[[habilitar \_ asignación](/windows/desktop/Midl/enable-allocate)\]                                  | Normalmente, ninguno. Sin embargo, el cliente puede usar un entorno de administración de memoria diferente.                                                     | El servidor usa un entorno de administración de memoria diferente. [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) debe usarse para las asignaciones. |
| \[[en](/windows/desktop/Midl/in) \] Atributo                                                    | Aplicación cliente responsable de asignar memoria para los datos.                                                                                 | Asignado en el servidor mediante código auxiliar.                                                                                                 |
| \[[out](/windows/desktop/Midl/out-idl) \] Atributo                                             | Asignado en el cliente mediante código auxiliar.                                                                                                                  | \[[out](/windows/desktop/Midl/out-idl) \] -only pointer must be \[ [ref](/windows/desktop/Midl/ref) \] pointer; allocated on server by stubs.                       |
| \[[ref](/windows/desktop/Midl/ref) \] Atributo                                                 | La aplicación cliente debe asignar la memoria a la que hace referencia el puntero.                                                                          | Punteros de referencia de nivel superior y de primer nivel administrados por códigos auxiliares.                                                                |
| \[[único](/windows/desktop/Midl/unique) \] Atributo                                           | Un valor distinto de NULL a NULL puede dar lugar a memoria huérfana; Null a non-null hace que el código auxiliar del cliente llame [a midl \_ user \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). | (Afecta al cliente).                                                                                                             |
| \[[ptr](/windows/desktop/Midl/ptr) \] Atributo                                                 | (Consulte \[ [único).](/windows/desktop/Midl/unique) \]                                                                                                              | (Consulte \[ [único).](/windows/desktop/Midl/unique) \]                                                                                             |



 

 

 