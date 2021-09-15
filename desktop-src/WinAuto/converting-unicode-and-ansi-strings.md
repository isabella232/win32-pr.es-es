---
title: Convertir cadenas Unicode y ANSI
description: Microsoft Active Accessibility usa cadenas Unicode definidas por el tipo de datos BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570049"
---
# <a name="converting-unicode-and-ansi-strings"></a>Convertir cadenas Unicode y ANSI

Microsoft Active Accessibility usa cadenas Unicode definidas por el **tipo de datos BSTR.** Si la aplicación no usa cadenas Unicode o si desea convertir cadenas para determinadas llamadas API, use las funciones [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) de Microsoft Win32 para realizar la conversión necesaria.

Use [**WideCharToMultiByte para**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) convertir una cadena Unicode en una cadena ANSI. La [**función MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) convierte una cadena ANSI en una cadena Unicode.

Use [**SysAllocString y**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) [**SysFreeString para**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) asignar y liberar tipos de datos **BSTR.**

Para obtener más información sobre estas funciones de cadena, vea sus referencias en el Kit de desarrollo de software (SDK) de Windows.

 

 