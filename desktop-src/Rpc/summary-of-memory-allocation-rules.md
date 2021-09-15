---
title: Resumen de reglas de asignación de memoria
description: En la tabla siguiente se resumen las reglas clave relativas a la asignación de memoria.
ms.assetid: 0c1f8398-75e6-45ec-a9f9-9dcdbe21c24d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9403bb5057b2004d966c0634bc101a3282fe92
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476599"
---
# <a name="summary-of-memory-allocation-rules"></a>Resumen de reglas de asignación de memoria

En la tabla siguiente se resumen las reglas clave relativas a la asignación de memoria.



| MidL, elemento                                                                                                                                           | Descripción                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Punteros \[ [de referencia de](/windows/desktop/Midl/ref) \] nivel superior                                                                                                                | Deben ser punteros no NULL.                                                                                                                                            |
| Valor devuelto de función                                                                                                                                  | Siempre se asigna nueva memoria para los valores devueltos del puntero.                                                                                                             |
| \[[unique](/windows/desktop/Midl/unique), [out](/windows/desktop/Midl/out-idl) \] o \[ [ptr](/windows/desktop/Midl/ptr), puntero \] out                                                                   | MIDL no permite.                                                                                                                                                  |
| Puntero único no de nivel superior , en , out o \[ [](/windows/desktop/Midl/unique) [](/windows/desktop/Midl/in) [](/windows/desktop/Midl/out-idl) \] \[ [ptr](/windows/desktop/Midl/ptr), en, puntero de salida que \] cambia de NULL a no NULL | Los códigos auxiliares de cliente asignan nueva memoria al cliente en la devolución.                                                                                                                 |
| Puntero no único de nivel \[ [](/windows/desktop/Midl/unique)superior , [en](/windows/desktop/Midl/in), puntero [de](/windows/desktop/Midl/out-idl) salida que cambia de \] distinto de NULL a NULL                                 | La memoria está huérfana en el cliente; la aplicación cliente es responsable de liberar memoria y evitar pérdidas.                                                              |
| ptr de nivel superior distinto \[ [de](/windows/desktop/Midl/ptr), [en](/windows/desktop/Midl/in), [puntero de](/windows/desktop/Midl/out-idl) salida que \] cambia de distinto de NULL a null                                       | La memoria estará huérfana en el cliente si no tiene alias; La aplicación cliente es responsable de liberar y evitar pérdidas de memoria en este caso.                             |
| \[[ref](/windows/desktop/Midl/ref) \] Punteros                                                                                                                           | El nivel de aplicación de cliente suele asignarse.                                                                                                                           |
| No null \[ [en ,](/windows/desktop/Midl/in) [puntero de](/windows/desktop/Midl/out-idl) \] salida                                                                                                | Los códigos auxiliares intentan escribir en el almacenamiento existente en el cliente. Si **\[ la cadena \]** y el tamaño aumentan más allá del tamaño asignado en el cliente, provocará un error de GP en la devolución. |



 

En la tabla siguiente se resumen los efectos de los atributos clave IDL y ACF en la administración de memoria.



| Característica MIDL                                                                   | Problemas del cliente                                                                                                                                  | Problemas del servidor                                                                                                                 |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \[[allocate](/windows/desktop/Midl/allocate)(nodo \_ único) \] , \[ allocate(all \_ nodes)\]         | Determina si se realizan una o varias llamadas a las funciones de memoria.                                                                         | Igual que el cliente, excepto la memoria privada que se puede usar a menudo para asignar (nodo \_ único) \[ en y en los datos de entrada y \] \[ \] salida.               |
| \[allocate(free) \] o \[ allocate(don't \_ free)\]                                 | (Ninguno; afecta al servidor).                                                                                                                        | Determina si la memoria del servidor se libera después de cada llamada a procedimiento remoto.                                            |
| El tamaño máximo \[ [de los atributos de \_ la matriz](/windows/desktop/Midl/max-is) \] es y el tamaño \[ [ \_ es](/windows/desktop/Midl/size-is)\] | (Ninguno; afecta al servidor).                                                                                                                        | Determina el tamaño de memoria que se va a asignar.                                                                                    |
| \[[recuento de \_ bytes](/windows/desktop/Midl/byte-count)\]                                            | El cliente debe asignar búfer; no se asignan ni liberan mediante código auxiliar de cliente.                                                                           | El atributo de parámetro ACF determina el tamaño del búfer asignado en el servidor.                                                        |
| \[[habilitar \_ asignación](/windows/desktop/Midl/enable-allocate)\]                                  | Normalmente, ninguno. Sin embargo, el cliente puede estar usando un entorno de administración de memoria diferente.                                                     | El servidor usa un entorno de administración de memoria diferente. [**RpcSmAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcsmallocate) debe usarse para las asignaciones. |
| \[[en](/windows/desktop/Midl/in) \] Atributo                                                    | Aplicación cliente responsable de asignar memoria para los datos.                                                                                 | Asignado en el servidor mediante código auxiliar.                                                                                                 |
| \[[out](/windows/desktop/Midl/out-idl) \] Atributo                                             | Asignado en el cliente mediante código auxiliar.                                                                                                                  | \[[out](/windows/desktop/Midl/out-idl) \] -only pointer must be \[ [ref](/windows/desktop/Midl/ref) \] pointer; allocated on server by stubs.                       |
| \[[ref](/windows/desktop/Midl/ref) \] Atributo                                                 | La aplicación cliente debe asignar la memoria a la que hace referencia el puntero.                                                                          | Punteros de referencia de nivel superior y de primer nivel administrados por código auxiliar.                                                                |
| \[[único](/windows/desktop/Midl/unique) \] Atributo                                           | Un valor distinto de NULL a NULL puede dar lugar a memoria huérfana; Null a non-null hace que el código auxiliar del cliente llame [a midl \_ user \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). | (Afecta al cliente).                                                                                                             |
| \[[ptr](/windows/desktop/Midl/ptr) \] Atributo                                                 | (Consulte \[ [único).](/windows/desktop/Midl/unique) \]                                                                                                              | (Consulte \[ [único).](/windows/desktop/Midl/unique) \]                                                                                             |



 

 

 