---
title: Códigos de error de Win32 para ADSI
description: Los códigos de error de Win32 estándar también se usan para devolver mensajes de error ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Códigos de error de Win32 para ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47151a3a1619a7f224dc0b9b7f0871813a346a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772883"
---
# <a name="win32-error-codes-for-adsi"></a>Códigos de error de Win32 para ADSI

Los códigos de error de Win32 estándar también se usan para devolver mensajes de error ADSI. En concreto, el proveedor LDAP de ADSI asigna todos los códigos de error LDAP a los códigos de error de Win32. Los valores **HRESULT** de estos códigos de error tienen el formato 0x8007XXXX, donde los últimos cuatro dígitos hexadecimales, xxxx, corresponden a los valores **DWORD** del código de error de Win32 adecuado. Por ejemplo, el valor de error de ADSI 0x80072020 proporciona el valor de error de Win32 de 0x2020 en formato hexadecimal o 8224 en formato decimal.

Para convertir el valor **HRESULT** de un código de error ADSI, devuelto por la aplicación, al valor **DWORD** del error de Win32 correspondiente, tal y como se define en los archivos de encabezado anteriores, utilice el procedimiento siguiente.

La mayoría de los códigos de error de Win32 para ADSI se definen en Winerror. h o Lmerr. h. Los valores de error se muestran como valores decimales en estos archivos.

**Para convertir el valor **HRESULT** de un código de error ADSI en el correspondiente valor **DWORD** de error de Win32**

1.  Convierta el valor **HRESULT** en un número hexadecimal si comienza con un valor decimal como puede obtener de una aplicación Visual Basic.
2.  Quitar el elemento 0x8007 produce el resto.
3.  Convierta el resto en un número decimal.
4.  Buscar el resto decimal en Winerror. h.
5.  Si no se encuentra en Winerror. h, reste 2100 del resto decimal y mire el resultado en Lmerr. h.

ADSI 2,0 asigna los códigos de error LDAP a un conjunto de códigos de error de Win32 que son diferentes de los que se usan en ADSI para Windows 2000 y el cliente DS. Las diferencias se enumeran en:

-   [Códigos de error de Win32](win32-error-codes.md)
-   [Códigos de error de Win32 para ADSI 2,0](win32-error-codes-for-adsi-2-0.md)

 

 




