---
description: Las funciones que no se han implementado con una versión Unicode normalmente se han reemplazado por funciones más eficaces o extendidas que admiten Unicode.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Usar funciones que no tienen equivalentes de Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0850eea442b98c81918c7c6733da65f730936be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279498"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a><span data-ttu-id="b8a9d-103">Usar funciones que no tienen equivalentes de Unicode</span><span class="sxs-lookup"><span data-stu-id="b8a9d-103">Using Functions That Have No Unicode Equivalents</span></span>

<span data-ttu-id="b8a9d-104">Las funciones que no se han implementado con una versión [Unicode](unicode.md) normalmente se han reemplazado por funciones más eficaces o extendidas que admiten Unicode.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-104">Functions that have not been implemented with a [Unicode](unicode.md) version have typically been replaced by more powerful or extended functions that do support Unicode.</span></span> <span data-ttu-id="b8a9d-105">Por ejemplo, si va a trasladar código que llama a la función [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) , la aplicación puede admitir Unicode mediante la función [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-105">For example, if you are porting code that calls the [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) function, your application can support Unicode by using the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function instead.</span></span>

<span data-ttu-id="b8a9d-106">Si una función no tiene ningún equivalente Unicode, la aplicación puede asignar caracteres a y desde juegos de caracteres de 8 bits antes y después de la llamada de función.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-106">If a function has no Unicode equivalent, the application can map characters to and from 8-bit character sets before and after the function call.</span></span> <span data-ttu-id="b8a9d-107">Por ejemplo, las funciones de formato de números **atoi** y **itoa** solo usan los dígitos del 0 al 9.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-107">For example, the number-formatting functions **atoi** and **itoa** use only the digits 0 through 9.</span></span> <span data-ttu-id="b8a9d-108">Normalmente, la asignación de Unicode a caracteres de 8 bits provoca la pérdida de datos, pero esto se puede evitar haciendo que el tipo de código sea independiente y haga que las expresiones sean condicionales.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-108">Normally, mapping Unicode to 8-bit characters causes loss of data, but this can be avoided by making the code type-independent and making the expressions conditional.</span></span> <span data-ttu-id="b8a9d-109">Las instrucciones del ejemplo siguiente, escritas para caracteres de 8 bits, son dependientes del tipo y deben cambiarse para admitir Unicode.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-109">The statements in the following example, written for 8-bit characters, are type-dependent and should be changed to support Unicode.</span></span>


```C++
char str[4] = "137";

int num = atoi(str);
```



<span data-ttu-id="b8a9d-110">Estas instrucciones se pueden volver a escribir de la siguiente manera para que sean independientes del tipo.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-110">These statements can be rewritten as follows to make them type-independent.</span></span>


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



<span data-ttu-id="b8a9d-111">En este ejemplo, la función de la biblioteca estándar de C **wcstombs** traduce Unicode a ASCII.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-111">In this example, the standard C library function **wcstombs** translates Unicode to ASCII.</span></span> <span data-ttu-id="b8a9d-112">El ejemplo se basa en el hecho de que los dígitos del 0 al 9 siempre se pueden traducir de Unicode a ASCII, incluso si parte del texto circundante no puede.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-112">The example relies on the fact that the digits 0 through 9 can always be translated from Unicode to ASCII, even if some of the surrounding text cannot.</span></span> <span data-ttu-id="b8a9d-113">La función **atoi** se detiene en cualquier carácter que no sea un dígito.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-113">The **atoi** function stops at any character that is not a digit.</span></span>

<span data-ttu-id="b8a9d-114">La aplicación puede utilizar la función de compatibilidad con National Language support (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) para procesar texto que incluye los [dígitos nativos](digit-shapes.md) proporcionados para algunos de los scripts de Unicode.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-114">Your application can use the National Language Support (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) function to process text that includes the [native digits](digit-shapes.md) provided for some of the scripts in Unicode.</span></span>

> [!Caution]  
> <span data-ttu-id="b8a9d-115">El uso incorrecto de la función **wcstombs** puede poner en peligro la seguridad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-115">Using the **wcstombs** function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="b8a9d-116">Asegúrese de que el búfer de aplicación para la cadena de caracteres de 8 bits sea al menos de tamaño \* 2 *( \_ longitud de char* + 1), donde la *\_ longitud de char* representa la longitud de la cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-116">Make sure that the application buffer for the string of 8-bit characters is at least of size 2\*(*char\_length* +1), where *char\_length* represents the length of the Unicode string.</span></span> <span data-ttu-id="b8a9d-117">Esta restricción se realiza porque, con [juegos de caracteres de doble byte](double-byte-character-sets.md) (DBCS), cada carácter Unicode se puede asignar a dos caracteres de 8 bits consecutivos.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-117">This restriction is made because, with [double-byte character sets](double-byte-character-sets.md) (DBCSs), each Unicode character can be mapped to two consecutive 8-bit characters.</span></span> <span data-ttu-id="b8a9d-118">Si el búfer no contiene toda la cadena, la cadena de resultado no termina en null, lo que plantea un riesgo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b8a9d-118">If the buffer does not hold the entire string, the result string is not null-terminated, posing a security risk.</span></span> <span data-ttu-id="b8a9d-119">Para obtener más información acerca de la seguridad de las aplicaciones, vea [consideraciones de seguridad: características internacionales](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="b8a9d-119">For more information about application security, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b8a9d-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b8a9d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8a9d-121">Usar Unicode y juegos de caracteres</span><span class="sxs-lookup"><span data-stu-id="b8a9d-121">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
