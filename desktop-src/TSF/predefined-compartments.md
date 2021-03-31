---
title: Compartimientos predefinidos (Ctffunc. h)
description: Los valores siguientes identifican los compartimientos implementados por el marco de trabajo de servicios de texto.
ms.assetid: 65177979-ff91-4f62-8ba5-3c426b221b6c
keywords:
- Marco de trabajo de servicios de texto de compartimientos predefinidos
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
ms.openlocfilehash: 9fcc684c4aee55c3c2e1807458ee261ad55156e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150856"
---
# <a name="predefined-compartments"></a>Compartimientos predefinidos

Los valores siguientes identifican los compartimientos implementados por el marco de trabajo de servicios de texto.

Los siguientes identificadores de compartimiento se definen en Ctffunc. idl y Ctffunc. h.



| Marca                                     | Value  | Descripción                                                                                                                                                                                                                                                                               |
|------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| compartimento de GUID de \_ \_ \_ audio SAPI           | VT \_ I4 | Un **valor DWORD** que es cero si el audio Speech API (SAPI) está desactivado o es distinto de cero si el audio SAPI está activado. Este compartimiento es específico de un objeto del administrador de subprocesos.                                                                                                                               |
| \_CFGMENU de \_ voz del compartimiento del GUID \_       | VT \_ I4 | Un **valor DWORD** que es cero si el menú de configuración de voz no está disponible o es distinto de cero si el menú de configuración de voz está disponible. Este compartimiento es específico de un objeto del administrador de subprocesos.                                                                                               |
| \_DICTATIONSTAT de \_ voz del compartimiento del GUID \_ | VT \_ I4 | Un valor **DWORD** que contiene cero o una combinación de uno o varios de los comandos TF [**\_ Dictation \_ Enabled**](speech-recognition-constants.md), **TF \_ Commanding \_ Enabled**, **TF \_ Dictation \_ on** o **TF \_ \_ en** los valores. Este compartimiento es específico de un objeto del administrador de subprocesos. |
| \_Estado de \_ UI de voz de compartimiento de GUID \_ \_    | VT \_ I4 | Un valor **DWORD** que contiene cero o una combinación de uno o varios de los valores [**TF \_ Show \_ Balloon**](speech-recognition-constants.md) o **TF \_ Disable \_ Balloon** . Se trata de un compartimiento global.                                                                                   |



 

Los siguientes identificadores de compartimiento se definen en MSCTF. IDL y MSCTF. H.



| Marca                                                    | Value  | Descripción                                                                                                                                                                                                                                                   |
|---------------------------------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_EMPTYCONTEXT de compartimiento de GUID \_                         | VT \_ I4 | Un **valor DWORD** que es distinto de cero si el contexto está vacío o cero en caso contrario. Este compartimiento es específico de un objeto de contexto.                                                                                                                                      |
| \_OPENCLOSE de \_ escritura a mano del compartimiento de GUID \_               | VT \_ I4 | Un **valor DWORD** que es distinto de cero si el reconocimiento de escritura a mano está abierto o cero si el reconocimiento de escritura a mano está cerrado. Este compartimiento es específico de un objeto del administrador de subprocesos.                                                                                 |
| teclado de compartimiento de GUID \_ \_ \_ deshabilitado                   | VT \_ I4 | Un **valor DWORD** que es distinto de cero si el teclado está deshabilitado o cero de lo contrario. Este compartimiento es específico de un objeto de contexto.                                                                                                                                  |
| \_conversión de \_ INPUTMODE de teclado del compartimiento de GUID \_ \_      | VT \_ I4 | Valor **DWORD** de la combinación adecuada de marcas [**TF \_ CONVERSIONMODE \_**](flags-for-conversion-mode.md) . Este compartimiento es específico de un objeto del administrador de subprocesos.                                                                                      |
| INPUTMODE de teclado de compartimiento de GUID ( \_ \_ \_ \_ oración)        | VT \_ I4 | Valor **DWORD** de [**TF \_ SENTENCEMODE \_**](flags-for-conversion-mode.md). Este compartimiento es específico de un objeto del administrador de subprocesos.                                                                                                                        |
| teclado de compartimiento de GUID \_ \_ \_ OPENCLOSE                  | VT \_ I4 | Un **valor DWORD** que es distinto de cero si el teclado está abierto o cero si el teclado está cerrado. Este compartimiento es específico de un objeto del administrador de subprocesos.                                                                                                               |
| \_PERSISTMENUENABLED de compartimiento de GUID \_                   | VT \_ I4 | Un **valor DWORD** que es distinto de cero para que el servicio de texto de voz habilite el elemento de menú **guardar datos de voz** o el valor cero para deshabilitarlo. Este compartimiento es específico de un objeto de administrador de documentos.                                                                   |
| voz de compartimiento de GUID \_ \_ \_ deshabilitada                     | VT \_ I4 | **DWORD** que contiene cero o una combinación de uno o varios de los valores de comandos TF Disable [**\_ \_ Speech**](speech-recognition-constants.md), TF Disable **\_ \_ dict** o **TF \_ Disable \_** . Este compartimiento es específico de un objeto del administrador de subprocesos. |
| \_OPENCLOSE de \_ voz del compartimiento del GUID \_                    | VT \_ I4 | Un **valor DWORD** que es distinto de cero si la entrada de voz está activa o es cero si la entrada de voz está inactiva. Se trata de un compartimiento global.                                                                                                                                      |
| \_TIPUISTATUS de compartimiento de GUID \_                          | VT \_ I4 | No se usa actualmente.                                                                                                                                                                                                                                           |
| \_TRANSITORYEXTENSION de compartimiento de GUID \_                  | VT \_ I4 | Un valor **DWORD** de [**TF \_ TRANSITORYEXTENSION \_ None**](values-for-guid-compartment-transitoryextension.md), **TF \_ TRANSITORYEXTENSION \_ float** o **TF \_ TRANSITORYEXTENSION \_ ATSELECTION**. Este compartimiento es específico de un objeto de administrador de documentos.  |
| DOCUMENTMANAGER de compartimiento de GUID \_ \_ TRANSITORYEXTENSION \_ | VT \_ I4 | Un valor IUnknown para la interfaz [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) que hace referencia al documento transitorio de este administrador de documentos. Este compartimiento es específico de un objeto de administrador de documentos.                                                         |
| \_ \_ TRANSITORYEXTENSION primario de compartimiento de GUID \_          | VT \_ I4 | Un valor IUnknown para la interfaz [**ITfDocumentMgr**](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) que hace referencia al administrador de documentos primario de este documento transitorio. Este compartimiento es específico de un objeto de administrador de documentos.                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Redistribuible<br/>          | TSF 1,0 en Windows 2000 Professional<br/>                                                                                                          |
| Encabezado<br/>                   | <dl> <dt>Ctffunc. h; </dt> <dt>Mstctf. h</dt> </dl>     |
| IDL<br/>                      | <dl> <dt>Ctffunc. idl; </dt> <dt>Mstctf. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Constantes de reconocimiento de voz**](speech-recognition-constants.md)
</dt> </dl>

 

 





