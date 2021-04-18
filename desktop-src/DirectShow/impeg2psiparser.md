---
description: La implementación de esta interfaz se proporciona como código de ejemplo con el SDK de DirectShow.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: Interfaz IMpeg2PsiParser
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
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677067"
---
# <a name="impeg2psiparser-interface"></a>Interfaz IMpeg2PsiParser

La implementación de esta interfaz se proporciona como código de ejemplo con el SDK de DirectShow. No es una API de DirectShow compatible.

La `IMpeg2PsiParser` interfaz recupera información específica del programa (PSI) del filtro del analizador de PSI, que se proporciona en el SDK de DirectShow como filtro de ejemplo. Una aplicación puede usar este filtro para asignar identificadores de programa (PID) en el filtro de demultiplexador MPEG-2.

## <a name="members"></a>Miembros

La interfaz **IMpeg2PsiParser** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMpeg2PsiParser** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMpeg2PsiParser** tiene estos métodos.



| Método                                                                             | Descripción                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))         | Busca el PID de la tabla de mapa de programas (PMT) para un programa, según el número de programa.<br/> |
| [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) | Recupera el número de flujos elementales en un programa especificado.<br/>             |
| [**GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md)                   | Recupera el número de programas en el flujo de transporte.<br/>                      |
| [**GetPatVersionNumber**](impeg2psiparser-getpatversionnumber.md)                 | Recupera el \_ campo de número de versión de la tabla de Asociación de programas (PAT).<br/>  |
| [**GetPmtVersionNumber**](impeg2psiparser-getpmtversionnumber.md)                 | Recupera el \_ campo de número de versión de un valor de PMT especificado.<br/>                      |
| [**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))           | Recupera la asignación de PID para una secuencia elemental especificada en un programa.<br/>   |
| [**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))           | Recupera la asignación de PID para un objeto PMT especificado.<br/>                              |
| [**GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)           | Recupera el número de programa para un programa especificado.<br/>                          |
| [**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))                 | Recupera el tipo de secuencia de una secuencia elemental especificada en un programa.<br/>      |
| [**GetTransportStreamId**](impeg2psiparser-gettransportstreamid.md)               | Recupera el \_ \_ campo de identificador de flujo de transporte de la Pat.<br/>                        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplo de filtro de analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 
