---
title: Valores devueltos por el administrador (msctf. h)
description: El marco de trabajo de servicios de texto genera valores devueltos en el intervalo de 0xHHHH0200 a 0xHHHH0507. En la tabla siguiente se proporciona al administrador los valores devueltos en orden alfabético.
ms.assetid: 12178252-c246-4fa4-bf7b-2445b859ec01
topic_type:
- apiref
api_name:
- Manager Return Values
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea9c813f9ba71371f45e2475f73af4f3016e17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535008"
---
# <a name="manager-return-values"></a>Valores devueltos por el administrador

El marco de trabajo de servicios de texto genera valores devueltos en el intervalo de 0x *hhhh* 0200 a 0x *hhhh* 0507. En la tabla siguiente se proporciona al administrador los valores devueltos en orden alfabético.

> [!Note]  
> Las descripciones proporcionadas no son específicas; el significado de un valor devuelto puede variar en función del método que devuelva el valor.

 



| Código o valor devuelto                                                                                                                                                                                                                                                   | Descripción                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="TF_E_ALREADY_EXISTS"></span><span id="tf_e_already_exists"></span><dl> <dt>**TF \_ E \_ ya \_ existe**</dt> <dt>0x80040506</dt> </dl>                   | La clave conservada está registrada.<br/>                                                       |
| <span id="TF_E_COMPOSITION_REJECTED"></span><span id="tf_e_composition_rejected"></span><dl> <dt>**TF \_ La \_ composición E \_ rechazó**</dt> <dt>0x80040508</dt> </dl> | El propietario del contexto rechazó la composición.<br/>                                            |
| <span id="TF_E_DISCONNECTED"></span><span id="tf_e_disconnected"></span><dl> <dt>**TF \_ E \_ 0x80040504 DESconectadas**</dt> <dt></dt> </dl>                          | El objeto de contexto no está en una pila de documentos.<br/>                                         |
| <span id="TF_E_EMPTYCONTEXT"></span><span id="tf_e_emptycontext"></span><dl> <dt>**TF \_ E \_ EMPTYCONTEXT**</dt> <dt>0x80040509</dt> </dl>                          | El contexto está vacío.<br/>                                                                  |
| <span id="TF_E_FORMAT"></span><span id="tf_e_format"></span><dl> <dt>**TF \_ \_Formato E**</dt> <dt>0x8004020a</dt> </dl>                                            | El propietario del contexto no puede controlar objetos del tipo proporcionado por el parámetro pDataObject.<br/> |
| <span id="TF_E_INVALIDPOINT"></span><span id="tf_e_invalidpoint"></span><dl> <dt>**TF \_ E \_ INVALIDPOINT**</dt> <dt>0x80040207</dt> </dl>                          | Las coordenadas de pantalla no son válidas.<br/>                                                    |
| <span id="TF_E_INVALIDPOS"></span><span id="tf_e_invalidpos"></span><dl> <dt>**TF \_ E \_ INVALIDPOS**</dt> <dt>0x80040200</dt> </dl>                                | La posición del carácter no es válida.<br/>                                                     |
| <span id="TF_E_INVALIDVIEW"></span><span id="tf_e_invalidview"></span><dl> <dt>**TF \_ E \_ INVALIDVIEW**</dt> <dt>0x80040505</dt> </dl>                             | La vista de contexto no es válida.<br/>                                                           |
| <span id="TF_E_LOCKED"></span><span id="tf_e_locked"></span><dl> <dt>**TF \_ E \_**</dt> <dt>0x80040500</dt> bloqueado </dl>                                            | El contexto ya está bloqueado.<br/>                                                         |
| <span id="TF_E_NOINTERFACE"></span><span id="tf_e_nointerface"></span><dl> <dt>**TF \_ E \_ nointerface**</dt> <dt>0x80040204</dt> </dl>                             | El objeto no admite la interfaz solicitada.<br/>                                   |
| <span id="TF_E_NOLAYOUT"></span><span id="tf_e_nolayout"></span><dl> <dt>**TF \_ E \_ nolayout**</dt> <dt>0x80040206</dt> </dl>                                      | No se ha calculado el diseño de texto.<br/>                                               |
| <span id="TF_E_NOLOCK"></span><span id="tf_e_nolock"></span><dl> <dt>**TF \_ E \_ NOLOCK**</dt> <dt>0x80040201</dt> </dl>                                            | El autor de la llamada no tiene el tipo de documento necesario.<br/>                               |
| <span id="TF_E_NOOBJECT"></span><span id="tf_e_noobject"></span><dl> <dt>**TF \_ E \_ noobject**</dt> <dt>0x80040202</dt> </dl>                                      | No existe ningún objeto incrustado en la posición especificada.<br/>                                   |
| <span id="TF_E_NOPROVIDER"></span><span id="tf_e_noprovider"></span><dl> <dt>**TF \_ E \_**</dt> <dt>no0x80040503</dt> </dl>                                | No existe ningún proveedor de funciones para la función especificada.<br/>                                |
| <span id="TF_E_NOSELECTION"></span><span id="tf_e_noselection"></span><dl> <dt>**TF \_ 0x80040205 \_ NOselect**</dt> <dt></dt> </dl>                             | No existe ninguna selección en el contexto.<br/>                                                |
| <span id="TF_E_NOSERVICE"></span><span id="tf_e_noservice"></span><dl> <dt>**TF \_ E \_ noservicio**</dt> <dt>0x80040203</dt> </dl>                                   | El servicio especificado no existe o no se puede crear.<br/>                            |
| <span id="TF_E_NOTOWNEDRANGE"></span><span id="tf_e_notownedrange"></span><dl> <dt>**TF \_ E \_ NOTOWNEDRANGE**</dt> <dt>0x80040502</dt> </dl>                       | El administrador de TSF no posee el intervalo.<br/>                                                |
| <span id="TF_E_RANGE_NOT_COVERED"></span><span id="tf_e_range_not_covered"></span><dl> <dt>**TF \_ \_Rango E \_ no \_ incluido**</dt> en <dt>0x80040507</dt> </dl>         | El intervalo no está dentro de una composición activa.<br/>                                         |
| <span id="TF_E_READONLY"></span><span id="tf_e_readonly"></span><dl> <dt>**TF \_ E \_ ReadOnly**</dt> <dt>0x80040209</dt> </dl>                                      | El contexto de edición es de solo lectura.<br/>                                                         |
| <span id="TF_E_STACKFULL"></span><span id="tf_e_stackfull"></span><dl> <dt>**TF \_ E \_ STACKFULL**</dt> <dt>0x80040501</dt> </dl>                                   | La pila de contexto está llena.<br/>                                                             |
| <span id="TF_E_SYNCHRONOUS"></span><span id="tf_e_synchronous"></span><dl> <dt>**TF \_ E \_ 0x80040208 sincrónicas**</dt> <dt></dt> </dl>                             | No se puede obtener un bloqueo sincrónico de solo lectura.<br/>                                       |
| <span id="TF_S_ASYNC"></span><span id="tf_s_async"></span><dl> <dt>**TF \_ S \_ Async**</dt> <dt>0x00040300</dt> </dl>                                               | Los datos se obtendrán de forma asincrónica.<br/>                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                      |
| Encabezado<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



 

 





