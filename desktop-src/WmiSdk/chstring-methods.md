---
description: La clase CHString expone los métodos siguientes.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Métodos CHString
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d15726702177aa484a070cca3ec1aab56d708b57991d3ff6a7aae43b1ccf68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556960"
---
# <a name="chstring-methods"></a>Métodos CHString

\[La [**clase CHString**](chstring.md) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

La [**clase CHString**](chstring.md) expone los métodos siguientes.

## <a name="in-this-section"></a>En esta sección

-   [**Método AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   [**Constructores CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))
-   [**Método Collate**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [**Compare (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [**Método CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [**Método vacío**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   [**Buscar métodos**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))
-   [**Método FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   [**Métodos de formato**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))
-   [**Métodos FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))
-   [**Método FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [**Método FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [**Método GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   [**Método GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))
-   [**GetBuffer (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [**Método GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [**Método GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [**Método GetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [**IsEmpty (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [**Método izquierdo**](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   [**Método LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))
-   [**Método LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [**Método MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [**Método MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [**Método MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   [**Métodos mid**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))
-   [**método \[ \] de operador**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))
-   [**CHString::operator+**](chstring--operator-plus.md)
-   [**CHString::operator+=**](chstring--operator-plus-equal.md)
-   [**CHString::operator=**](chstring--operator-equal.md)
-   [**Operator==(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))
-   [**operator==(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))
-   [**Operator>(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))
-   [**operator>(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))
-   [**operator>=(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))
-   [**operator>=(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))
-   [**Operator<(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))
-   [**operator<(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))
-   [**operator<=(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))
-   [**operator<=(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))
-   [**operator!=(constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))
-   [**operator!=(constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))
-   [**Método LPCWSTR del operador**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [**Método ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [**Método ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [**Método correcto**](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [**Método SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [**Método SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [**Método SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [**Método TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [**TrimRight (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [**Método UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
