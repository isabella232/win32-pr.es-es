---
title: Consideraciones sobre Unicode
description: La función de servicio WriteFmtUserTypeStg, que se usa en el método IPaper Save, requiere parámetros de cadena Unicode.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06f8fa9592d3f29ccf82d42f38a48b2dc57d36bccf79b22b8fe159bad337cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886743"
---
# <a name="unicode-considerations"></a>Consideraciones sobre Unicode

La **función de servicio WriteFmtUserTypeStg,** que se usa en el método [**IPaper::Save,**](ipaper--save.md) requiere parámetros de cadena Unicode. Este es el caso de las llamadas de servicio COM/OLE que toman parámetros de cadena. Al compilar para cadenas ANSI, los parámetros Unicode esperados necesitan la conversión de ANSI a Unicode. Este proceso se logra mediante algunas macros de APPUTIL.h que pueden ocultar las conversiones. Por ejemplo, vea **WriteFmtUserTypeStg**.

La siguiente llamada aparece en el [**método Save.**](ipaper--save.md)


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



Cuando **StoServe se** compila para ANSI (no para Unicode), esta llamada se reduce realmente a una llamada a una función suplente APPUTIL interna. Para admitir esto, se usa el siguiente esquema de macro en Apputil.h, que es un archivo incluido en todos los ejemplos de código . Archivos CPP.


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



El esquema usa funciones de llamada de servicio suplentes. Las versiones ANSI de las llamadas comienzan por A \_ . Estas funciones ANSI suplentes se implementan en Apputil.cpp. Se usan cuando se compila el ejemplo de código para cadenas ANSI (el valor predeterminado en los archivos Make). Las funciones de servicio que los suplentes están en lugar de admitir solo parámetros de cadena Unicode. Esto fuerza algunas conversiones de cadenas de ANSI a Unicode antes de que la llamada real al servicio COM/OLE se realiza dentro del suplente.

Por ejemplo, si no se define UNICODE durante la compilación, las macros cambian realmente las llamadas de los ejemplos a la función de servicio COM **WriteFmtUserTypeStg** en llamadas a una función WriteFmtUserTypeStg que se implementa en \_ APPUTIL. Cpp. Esta función acepta el puntero de cadena ANSI de entrada, lo convierte en una copia Unicode y pasa esa copia Unicode como parámetro de cadena en una llamada a la función **WriteFmtUserTypeStg** real.

Este es un \_ writefmtUserTypeStg de Apputil.cpp.

``` syntax
STDAPI A_WriteFmtUserTypeStg(
           IStorage* pIStorage,
           CLIPFORMAT ClipFmt,
           LPSTR pszUserType)
  {
    HRESULT hr = E_INVALIDARG;
    WCHAR wszUc[MAX_PATH];

    if (NULL != pszUserType)
    {
      // Convert from ANSI in pszUserType to Unicode in wszUc.
      AnsiToUc(pszUserType, wszUc, MAX_PATH);

      // Use the Unicode string in the actual service call.
      hr = WriteFmtUserTypeStg(pIStorage, ClipFmt, wszUc);
    }

    return hr;
  }
```

 

 




