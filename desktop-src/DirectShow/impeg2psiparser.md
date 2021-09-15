---
description: La implementación de esta interfaz se proporciona como código de ejemplo con DirectShow SDK.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: IMpeg2PsiParser (interfaz)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473981"
---
# <a name="impeg2psiparser-interface"></a>IMpeg2PsiParser (interfaz)

La implementación de esta interfaz se proporciona como código de ejemplo con DirectShow SDK. No es una API de DirectShow compatible.

La interfaz recupera información específica del programa (PSI) del filtro analizador de PSI, que se proporciona en el SDK de DirectShow `IMpeg2PsiParser` como filtro de ejemplo. Una aplicación puede usar este filtro para asignar los ID de programa (PID) en el filtro Demultiplexer MPEG-2.

## <a name="members"></a>Members

La **interfaz IMpeg2PsiParser** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMpeg2PsiParser** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMpeg2PsiParser** tiene estos métodos.



| Método                                                                             | Descripción                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))         | Busca el PID de la tabla de asignación de programas (PMT) de un programa, dado el número de programa.<br/> |
| [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) | Recupera el número de secuencias elementales de un programa especificado.<br/>             |
| [**GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md)                   | Recupera el número de programas de la secuencia de transporte.<br/>                      |
| [**GetPatVersionNumber**](impeg2psiparser-getpatversionnumber.md)                 | Recupera el campo número \_ de versión de la tabla de asociación de programas (PAT).<br/>  |
| [**GetPmtVersionNumber**](impeg2psiparser-getpmtversionnumber.md)                 | Recupera el campo de \_ número de versión de un PMT especificado.<br/>                      |
| [**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))           | Recupera la asignación de PID para una secuencia primaria especificada en un programa.<br/>   |
| [**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))           | Recupera la asignación de PID para un PMT especificado.<br/>                              |
| [**GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)           | Recupera el número de programa de un programa especificado.<br/>                          |
| [**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))                 | Recupera el tipo de secuencia para una secuencia primaria especificada en un programa.<br/>      |
| [**GetTransportStreamId**](impeg2psiparser-gettransportstreamid.md)               | Recupera el campo de \_ \_ id. de flujo de transporte del PAT.<br/>                        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplo de filtro del analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 
