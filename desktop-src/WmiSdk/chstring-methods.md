---
description: La clase CHString expone los métodos siguientes.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Métodos CHString
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15a26bf2b5945990f8cd37ee67c2953395ca98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082866"
---
# <a name="chstring-methods"></a>Métodos CHString

\[La clase [**CHString**](chstring.md) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

La clase [**CHString**](chstring.md) expone los métodos siguientes.

## <a name="in-this-section"></a>En esta sección

-   [**Método AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   [**Constructores CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))
-   [**COLLATE (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [**Compare (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [**Método CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [**Empty (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   [**Métodos de búsqueda**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))
-   [**Método FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   [**Métodos de formato**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))
-   [**Métodos FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))
-   [**Método FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [**Método FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [**Método GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   [**GetAt (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))
-   [**GetBuffer (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [**Método GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [**Método GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [**GetLength (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [**IsEmpty (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [**Left (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   [**Método LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))
-   [**Método LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [**Método MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [**Método MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [**Método MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   [**Métodos MID**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))
-   [**Operator ( \[ \] método)**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))
-   [**CHString:: Operator +**](chstring--operator-plus.md)
-   [**CHString:: Operator + =**](chstring--operator-plus-equal.md)
-   [**CHString:: Operator =**](chstring--operator-equal.md)
-   [**Operator = = (constCHString&, constCHString&) (método)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))
-   [**Operator = = (constCHString&, constLPCWSTR&) (método)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))
-   [**Operator> (método constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))
-   [**Operator> (método constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))
-   [**Operator>= (constCHString&, constCHString&) (método)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))
-   [**Operator>= (constCHString&, constLPCWSTR&) (método)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))
-   [**Operator< (método constCHString&, constCHString&)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))
-   [**Operator< (método constCHString&, constLPCWSTR&)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))
-   [**Operator<= (constCHString&, constCHString&) (método)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))
-   [**Operator<= (constCHString&, constLPCWSTR&) (método)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))
-   [**Operator! = (constCHString&, constCHString&) (método)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))
-   [**Operator! = (constCHString&, constLPCWSTR&) (método)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))
-   [**Operator LPCWSTR (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [**Método ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [**Método ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [**Right (método)**](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [**Método SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [**Método SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [**Método SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [**Método TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [**Método TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [**Método UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
