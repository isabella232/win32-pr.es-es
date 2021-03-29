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
# <a name="unicode-considerations"></a><span data-ttu-id="53adf-103">Consideraciones de Unicode</span><span class="sxs-lookup"><span data-stu-id="53adf-103">Unicode Considerations</span></span>

<span data-ttu-id="53adf-104">La función de servicio **WriteFmtUserTypeStg** , que se usa en el método [**IPaper:: Save**](ipaper--save.md) , requiere parámetros de cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="53adf-104">The **WriteFmtUserTypeStg** service function, used in the [**IPaper::Save**](ipaper--save.md) method, requires Unicode string parameters.</span></span> <span data-ttu-id="53adf-105">Este es el caso de las llamadas al servicio COM/OLE que toman parámetros de cadena.</span><span class="sxs-lookup"><span data-stu-id="53adf-105">This is the case with COM/OLE service calls that take string parameters.</span></span> <span data-ttu-id="53adf-106">Al compilar para cadenas ANSI, los parámetros Unicode esperados necesitan la conversión de ANSI a Unicode.</span><span class="sxs-lookup"><span data-stu-id="53adf-106">When compiling for ANSI strings, the expected Unicode parameters need conversion from ANSI to Unicode.</span></span> <span data-ttu-id="53adf-107">Este proceso se consigue mediante el uso de algunas macros de APPUTIL. h que podrían ocultar las conversiones.</span><span class="sxs-lookup"><span data-stu-id="53adf-107">This process is achieved using some macros in APPUTIL.h that may obscure conversions.</span></span> <span data-ttu-id="53adf-108">Por ejemplo, vea **WriteFmtUserTypeStg**.</span><span class="sxs-lookup"><span data-stu-id="53adf-108">For example, see **WriteFmtUserTypeStg**.</span></span>

<span data-ttu-id="53adf-109">La llamada siguiente aparece en el método [**Save**](ipaper--save.md) .</span><span class="sxs-lookup"><span data-stu-id="53adf-109">The following call appears in the [**Save**](ipaper--save.md) method.</span></span>


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



<span data-ttu-id="53adf-110">Cuando **StoServe** se COMPILA para ANSI (no para Unicode), esta llamada se reduce realmente a una llamada a una función suplente APPUTIL interna.</span><span class="sxs-lookup"><span data-stu-id="53adf-110">When **StoServe** is compiled for ANSI (not for Unicode), this call actually reduces to a call to an internal APPUTIL surrogate function.</span></span> <span data-ttu-id="53adf-111">Para admitir esto, se usa el siguiente esquema de macro en apputil. h, que es un archivo incluido en todo el ejemplo de código. Archivos CPP.</span><span class="sxs-lookup"><span data-stu-id="53adf-111">To support this, the following macro scheme is used in Apputil.h, which is an included file in all code sample .CPP files.</span></span>


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



<span data-ttu-id="53adf-112">El esquema utiliza funciones de llamada de servicio suplente.</span><span class="sxs-lookup"><span data-stu-id="53adf-112">The scheme uses surrogate service call functions.</span></span> <span data-ttu-id="53adf-113">Las versiones ANSI de las llamadas comienzan por \_ .</span><span class="sxs-lookup"><span data-stu-id="53adf-113">The ANSI versions of the calls begin with A\_.</span></span> <span data-ttu-id="53adf-114">Estas funciones ANSI Suplentes se implementan en apputil. cpp.</span><span class="sxs-lookup"><span data-stu-id="53adf-114">These surrogate ANSI functions are implemented in Apputil.cpp.</span></span> <span data-ttu-id="53adf-115">Se usan cuando se compila el ejemplo de código para cadenas ANSI (el valor predeterminado en los archivos make).</span><span class="sxs-lookup"><span data-stu-id="53adf-115">They are used when the code sample is being compiled for ANSI strings (the default in the makefiles).</span></span> <span data-ttu-id="53adf-116">Las funciones de servicio que se aplican a los suplentes solo admiten parámetros de cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="53adf-116">The service functions that the surrogates stand in place of support only Unicode string parameters.</span></span> <span data-ttu-id="53adf-117">Esto fuerza a algunas conversiones de cadenas de ANSI a Unicode antes de que se realice la llamada al servicio COM/OLE real dentro del suplente.</span><span class="sxs-lookup"><span data-stu-id="53adf-117">This forces some string conversions from ANSI to Unicode before the real COM/OLE service call is made inside the surrogate.</span></span>

<span data-ttu-id="53adf-118">Por ejemplo, si no se define Unicode durante la compilación, las llamadas de los ejemplos a la función de servicio com **WriteFmtUserTypeStg** realmente las cambian las macros en llamadas a una \_ función WriteFmtUserTypeStg que se implementa en apputil. CPP.</span><span class="sxs-lookup"><span data-stu-id="53adf-118">For example, if UNICODE is not defined during compiling, any calls in the samples to the **WriteFmtUserTypeStg** COM service function are actually changed by the macros into calls to an A\_WriteFmtUserTypeStg function that is implemented in APPUTIL.CPP.</span></span> <span data-ttu-id="53adf-119">Esta función acepta el puntero de cadena ANSI de entrada, lo convierte en una copia Unicode y pasa esa copia Unicode como parámetro de cadena en una llamada a la función **WriteFmtUserTypeStg** real.</span><span class="sxs-lookup"><span data-stu-id="53adf-119">This function accepts the input ANSI string pointer, converts it to a Unicode copy, and passes that Unicode copy as the string parameter in a call to the actual **WriteFmtUserTypeStg** function.</span></span>

<span data-ttu-id="53adf-120">A continuación se muestra un \_ WriteFmtUserTypeStg de APPUTIL. cpp.</span><span class="sxs-lookup"><span data-stu-id="53adf-120">Here is A\_WriteFmtUserTypeStg from Apputil.cpp.</span></span>

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

 

 




