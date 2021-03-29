---
title: Consideraciones de Unicode
description: La función de servicio WriteFmtUserTypeStg, que se usa en el método Save de IPaper, requiere parámetros de cadena Unicode.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7bef75ec88318f4a2af8c5c7b693f0fc7c877f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903489"
---
# <a name="unicode-considerations"></a>Consideraciones de Unicode

La función de servicio **WriteFmtUserTypeStg** , que se usa en el método [**IPaper:: Save**](ipaper--save.md) , requiere parámetros de cadena Unicode. Este es el caso de las llamadas al servicio COM/OLE que toman parámetros de cadena. Al compilar para cadenas ANSI, los parámetros Unicode esperados necesitan la conversión de ANSI a Unicode. Este proceso se consigue mediante el uso de algunas macros de APPUTIL. h que podrían ocultar las conversiones. Por ejemplo, vea **WriteFmtUserTypeStg**.

La llamada siguiente aparece en el método [**Save**](ipaper--save.md) .


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



Cuando **StoServe** se COMPILA para ANSI (no para Unicode), esta llamada se reduce realmente a una llamada a una función suplente APPUTIL interna. Para admitir esto, se usa el siguiente esquema de macro en apputil. h, que es un archivo incluido en todo el ejemplo de código. Archivos CPP.


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



El esquema utiliza funciones de llamada de servicio suplente. Las versiones ANSI de las llamadas comienzan por \_ . Estas funciones ANSI Suplentes se implementan en apputil. cpp. Se usan cuando se compila el ejemplo de código para cadenas ANSI (el valor predeterminado en los archivos make). Las funciones de servicio que se aplican a los suplentes solo admiten parámetros de cadena Unicode. Esto fuerza a algunas conversiones de cadenas de ANSI a Unicode antes de que se realice la llamada al servicio COM/OLE real dentro del suplente.

Por ejemplo, si no se define Unicode durante la compilación, las llamadas de los ejemplos a la función de servicio com **WriteFmtUserTypeStg** realmente las cambian las macros en llamadas a una \_ función WriteFmtUserTypeStg que se implementa en apputil. CPP. Esta función acepta el puntero de cadena ANSI de entrada, lo convierte en una copia Unicode y pasa esa copia Unicode como parámetro de cadena en una llamada a la función **WriteFmtUserTypeStg** real.

A continuación se muestra un \_ WriteFmtUserTypeStg de APPUTIL. cpp.

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

 

 




