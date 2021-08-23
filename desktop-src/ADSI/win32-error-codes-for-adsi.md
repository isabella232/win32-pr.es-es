---
title: Códigos de error de Win32 para ADSI
description: Los códigos de error Estándar Win32 también se usan para devolver mensajes de error ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Códigos de error de Win32 para ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b18539e93504991f244bbba8b41b13e524ff236918145deda73788169cef368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589745"
---
# <a name="win32-error-codes-for-adsi"></a>Códigos de error de Win32 para ADSI

Los códigos de error Estándar Win32 también se usan para devolver mensajes de error ADSI. En concreto, el proveedor LDAP ADSI asigna todos los códigos de error LDAP a códigos de error de Win32. Los **valores HRESULT** de estos códigos de error tienen el formato 0x8007XXXX, donde los cuatro últimos dígitos hexadecimales, XXXX, corresponden a los valores **DWORD** del código de error win32 adecuado. Por ejemplo, el valor de error ADSI 0x80072020 el valor de error de Win32 0x2020 en hexadecimal o 8224 en decimal.

Para convertir el valor **HRESULT** de un código de error ADSI, devuelto por la aplicación, en el valor **DWORD** de error de Win32 correspondiente, tal como se define en los archivos de encabezado anteriores, use el procedimiento siguiente.

La mayoría de los códigos de error de Win32 para ADSI se definen en Winerror.h o Lmerr.h. Los valores de error se muestran como valores decimales en estos archivos.

**Para convertir el **valor HRESULT** de un código de error ADSI en el valor **DWORD** de error de Win32 correspondiente**

1.  Convierta el **valor HRESULT** en un número hexadecimal si empieza con un valor decimal como puede obtener de una Visual Basic aplicación.
2.  Al quitar el 0x8007 parte se produce el resto.
3.  Convierta el resto en un número decimal.
4.  Busque el resto decimal en Winerror.h.
5.  Si no se encuentra en Winerror.h, resta 2100 del resto decimal y busca el resultado en Lmerr.h.

ADSI 2.0 asigna los códigos de error LDAP a un conjunto de códigos de error de Win32 que es diferente del usado en ADSI para Windows 2000 y DS Client. Las diferencias se enumeran en:

-   [Códigos de error de Win32](win32-error-codes.md)
-   [Códigos de error de Win32 para ADSI 2.0](win32-error-codes-for-adsi-2-0.md)

 

 




