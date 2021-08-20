---
description: La implementación de esta interfaz se proporciona como código de ejemplo con DirectShow SDK.
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
ms.openlocfilehash: e426dee9d60344e2167169533bf80ee3e42f7403a52e3b90d844175d4c219075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998106"
---
# <a name="impeg2psiparser-interface"></a>Interfaz IMpeg2PsiParser

La implementación de esta interfaz se proporciona como código de ejemplo con DirectShow SDK. No se admite DirectShow API.

La interfaz recupera información específica del programa (PSI) del filtro analizador de PSI, que se proporciona en el SDK de DirectShow `IMpeg2PsiParser` como filtro de ejemplo. Una aplicación puede usar este filtro para asignar los ID de programa (PID) en el filtro de demultiplexor MPEG-2.

## <a name="members"></a>Miembros

La **interfaz IMpeg2PsiParser** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMpeg2PsiParser** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMpeg2PsiParser** tiene estos métodos.



| Método                                                                             | Descripción                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))         | Busca el PID de tabla de asignación de programas (PMT) de un programa, según el número de programa.<br/> |
| [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) | Recupera el número de secuencias elementales de un programa especificado.<br/>             |
| [**GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md)                   | Recupera el número de programas de la secuencia de transporte.<br/>                      |
| [**GetPatVersionNumber**](impeg2psiparser-getpatversionnumber.md)                 | Recupera el campo número \_ de versión de la tabla de asociación de programas (PAT).<br/>  |
| [**GetPmtVersionNumber**](impeg2psiparser-getpmtversionnumber.md)                 | Recupera el campo de \_ número de versión de un PMT especificado.<br/>                      |
| [**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))           | Recupera la asignación de PID para una secuencia elemental especificada en un programa.<br/>   |
| [**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))           | Recupera la asignación de PID para un PMT especificado.<br/>                              |
| [**GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)           | Recupera el número de programa de un programa especificado.<br/>                          |
| [**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))                 | Recupera el tipo de secuencia para una secuencia elemental especificada en un programa.<br/>      |
| [**GetTransportStreamId**](impeg2psiparser-gettransportstreamid.md)               | Recupera el campo de \_ \_ id. de flujo de transporte del PAT.<br/>                        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplo de filtro del analizador de PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 
