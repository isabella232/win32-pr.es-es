---
title: Convertir cadenas ANSI y Unicode
description: Microsoft Active Accessibility usa cadenas Unicode, tal y como se define en el tipo de datos BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359190"
---
# <a name="converting-unicode-and-ansi-strings"></a>Convertir cadenas ANSI y Unicode

Microsoft Active Accessibility usa cadenas Unicode, tal y como se define en el tipo de datos **BSTR** . Si la aplicación no usa cadenas Unicode, o si desea convertir cadenas para determinadas llamadas API, use las funciones de Microsoft Win32 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para realizar la conversión necesaria.

Use [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para convertir una cadena Unicode en una cadena ANSI. La función [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) convierte una cadena ANSI en una cadena Unicode.

Use [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) y [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) para asignar y liberar tipos de datos **BSTR** .

Para obtener más información sobre estas funciones de cadena, vea sus referencias en el kit de desarrollo de software (SDK) de Windows.

 

 