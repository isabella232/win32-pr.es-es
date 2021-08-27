---
title: Compartimientos predefinidos (Ctffunc.h)
description: Los valores siguientes identifican los compartimientos implementados por Text Services Framework.
ms.assetid: 65177979-ff91-4f62-8ba5-3c426b221b6c
keywords:
- Compartimientos predefinidos Text Services Framework
topic_type:
- apiref
api_name:
- Predefined Compartments
api_location:
- Ctffunc.h
- Mstctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7c59312f7511c093f0d4c51bbdb9491f44b17cd16475e2b4261eaa676836e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118876187"
---
# <a name="predefined-compartments"></a>Compartimientos predefinidos

Los valores siguientes identifican los compartimientos implementados por Text Services Framework.

Los siguientes identificadores de compartimiento se definen en Ctffunc.idl y Ctffunc.h.



| Marca                                     | Value  | Descripción                                                                                                                                                                                                                                                                               |
|------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AUDIO \_ \_ SAPI DEL COMPARTIMIENTO \_ GUID           | VT \_ I4 | DWORD **que** es cero si el audio Speech API (SAPI) está desactivado o es distinto de cero si el audio SAPI está activada. Este compartimiento es específico de un objeto de administrador de subprocesos.                                                                                                                               |
| GUID \_ COMPARTMENT \_ SPEECH \_ CFGMENU       | VT \_ I4 | DWORD **que es** cero si el menú de configuración de voz no está disponible o es distinto de cero si el menú de configuración de voz está disponible. Este compartimiento es específico de un objeto de administrador de subprocesos.                                                                                               |
| GUID \_ COMPARTMENT \_ SPEECH \_ DICTATIONSTAT | VT \_ I4 | Valor **DWORD** que contiene cero o una combinación de uno o varios de los valores [**TF \_ DICTATION \_ ENABLED**](speech-recognition-constants.md), **TF \_ COMMANDING \_ ENABLED,** **TF \_ DICTATION \_ ON** o **TF \_ COMMANDING \_ ON.** Este compartimiento es específico de un objeto de administrador de subprocesos. |
| ESTADO DE \_ LA INTERFAZ DE USUARIO DE VOZ DEL COMPARTIMIENTO \_ \_ \_ GUID    | VT \_ I4 | Valor **DWORD que** contiene cero o una combinación de uno o varios de los valores [**TF SHOW \_ \_ BALLOON**](speech-recognition-constants.md) o **TF DISABLE \_ \_ BALLOON.** Se trata de un compartimiento global.                                                                                   |



 

Los siguientes identificadores de compartimiento se definen en MSCTF. IDL y MSCTF.H.



| Marca                                                    | Value  | Descripción                                                                                                                                                                                                                                                   |
|---------------------------------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID \_ COMPARTMENT \_ EMPTYCONTEXT                         | VT \_ I4 | DWORD **que** es distinto de cero si el contexto está vacío o cero en caso contrario. Este compartimiento es específico de un objeto de contexto.                                                                                                                                      |
| GUID \_ COMPARTMENT \_ HANDWRITING \_ OPENCLOSE               | VT \_ I4 | DWORD **que es** distinto de cero si el reconocimiento de escritura a mano está abierto o cero si el reconocimiento de escritura a mano está cerrado. Este compartimiento es específico de un objeto de administrador de subprocesos.                                                                                 |
| TECLADO DEL \_ COMPARTIMIENTO \_ GUID \_ DESHABILITADO                   | VT \_ I4 | DWORD **que** es distinto de cero si el teclado está deshabilitado o cero en caso contrario. Este compartimiento es específico de un objeto de contexto.                                                                                                                                  |
| CONVERSIÓN \_ \_ \_ INPUTMODE DEL TECLADO DEL COMPARTIMIENTO \_ GUID      | VT \_ I4 | Valor **DWORD** de la combinación adecuada de [**marcas \_ CONVERSIONMODE de \_ TF.**](flags-for-conversion-mode.md) Este compartimiento es específico de un objeto de administrador de subprocesos.                                                                                      |
| ORACIÓN \_ \_ \_ INPUTMODE DEL TECLADO DEL COMPARTIMIENTO \_ GUID        | VT \_ I4 | Valor **DWORD** de [**TF \_ SENTENCEMODE. \_**](flags-for-conversion-mode.md) Este compartimiento es específico de un objeto de administrador de subprocesos.                                                                                                                        |
| TECLADO \_ DE COMPARTIMIENTO GUID \_ \_ OPENCLOSE                  | VT \_ I4 | DWORD **que** es distinto de cero si el teclado está abierto o cero si el teclado está cerrado. Este compartimiento es específico de un objeto de administrador de subprocesos.                                                                                                               |
| GUID \_ COMPARTMENT \_ PERSISTMENUENABLED                   | VT \_ I4 | Un **DWORD distinto** de cero para que el servicio de texto de voz habilite el elemento de menú **Guardar** datos de voz o cero para deshabilitarlo. Este compartimiento es específico de un objeto de administrador de documentos.                                                                   |
| GUID \_ COMPARTMENT \_ SPEECH \_ DISABLED                     | VT \_ I4 | DWORD **que contiene** cero o una combinación de uno o varios de los valores DISABLE [**\_ \_ SPEECH**](speech-recognition-constants.md)de **TF, TF \_ DISABLE \_ DICTATION** o **TF DISABLE \_ \_ COMMANDING.** Este compartimiento es específico de un objeto de administrador de subprocesos. |
| GUID \_ COMPARTMENT \_ SPEECH \_ OPENCLOSE                    | VT \_ I4 | DWORD **que es** distinto de cero si la entrada de voz está activa o cero si la entrada de voz está inactiva. Se trata de un compartimiento global.                                                                                                                                      |
| GUID \_ COMPARTMENT \_ TIPUISTATUS                          | VT \_ I4 | No se usa actualmente.                                                                                                                                                                                                                                           |
| \_ \_ TRANSITORYEXTENSION DEL COMPARTIMIENTO GUID                  | VT \_ I4 | Valor **DWORD de** [**TF \_ TRANSITORYEXTENSION \_ NONE**](values-for-guid-compartment-transitoryextension.md), **TF \_ TRANSITORYEXTENSION \_ FLOATING** o **TF \_ TRANSITORYEXTENSION \_ ATSELECTION**. Este compartimiento es específico de un objeto de administrador de documentos.  |
| GUID \_ COMPARTMENT \_ TRANSITORYEXTENSION \_ DOCUMENTMANAGER | VT \_ I4 | Valor IUnknown para la [**interfaz ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) que hace referencia al documento transitorio de este administrador de documentos. Este compartimiento es específico de un objeto de administrador de documentos.                                                         |
| ELEMENTO PRIMARIO \_ \_ TRANSITORYEXTENSION DEL COMPARTIMIENTO \_ GUID          | VT \_ I4 | Valor IUnknown para la [**interfaz ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) que hace referencia al administrador de documentos primarios de este documento transitorio. Este compartimiento es específico de un objeto de administrador de documentos.                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Redistribuible<br/>          | TSF 1.0 en Windows 2000 Professional<br/>                                                                                                          |
| Header<br/>                   | <dl> <dt>Ctffunc.h; </dt> <dt>Mstctf.h</dt> </dl>     |
| Idl<br/>                      | <dl> <dt>Ctffunc.idl; </dt> <dt>Mstctf.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Constantes de reconocimiento de voz**](speech-recognition-constants.md)
</dt> </dl>

 

 





