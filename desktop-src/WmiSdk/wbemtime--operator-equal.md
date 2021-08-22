---
description: Los operadores de asignación de clases WBEMTime se sobrecargan para facilitar las conversiones entre varios formatos de tiempo de ejecución Windows y ANSI C. A continuación se enumeran las distintas firmas sobrecargadas.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: Operadores WBEMTime::operator= (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 321ca0ba75d40389fbd6eb2ba70dc67a9b8e16afd3b5390bbc9ec61bd875c79a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502905"
---
# <a name="wbemtimeoperator-operators"></a>Operadores WBEMTime::operator=

\[La [**clase WBEMTime**](wbemtime.md) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

Los operadores de asignación de clases [**WBEMTime**](wbemtime.md) se sobrecargan para facilitar las conversiones entre varios formatos Windows y ANSI C en tiempo de ejecución. A continuación se enumeran las distintas firmas sobrecargadas.

### <a name="overload-list"></a>Lista de sobrecarga



| Operador                                                                     | Descripción                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**operator=(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | Convierte un **BSTR al** **formato WBEMTime.**<br/>         |
| [**operator=(time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | Convierte la **hora \_ t al** formato **WBEMTime.**<br/>        |
| [**operator=(FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | Convierte **FILETIME al** **formato WBEMTime.**<br/>       |
| [**operator=(struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | Convierte una estructura **tm** al **formato WBEMTime.**<br/> |
| [**operator=(SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | Convierte **SYSTEMTIME al** **formato WBEMTime.**<br/>     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
