---
title: IAgentCharacterEx GetAnimationNames
description: IAgentCharacterEx GetAnimationNames
ms.assetid: d565b258-dc12-422b-a13d-aeec56057f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31dcb7ea34a9f0d833f8c1665a092fe4f3a30e7
ms.sourcegitcommit: baa7cd1709e48672f5f07ff83a9c9d5699c0efcd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "105697896"
---
# <a name="iagentcharacterexgetanimationnames"></a><span data-ttu-id="66da7-103">IAgentCharacterEx::GetAnimationNames</span><span class="sxs-lookup"><span data-stu-id="66da7-103">IAgentCharacterEx::GetAnimationNames</span></span>

<span data-ttu-id="66da7-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="66da7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAnimationNames(
   IUnknown ** punkEnum // address of IUnknown interface
);
```

<span data-ttu-id="66da7-105">Recupera los nombres de animación de un carácter.</span><span class="sxs-lookup"><span data-stu-id="66da7-105">Retrieves the animation names for a character.</span></span>

-   <span data-ttu-id="66da7-106">Devuelve **S \_ OK** para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="66da7-106">Returns **S\_OK** to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="66da7-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="66da7-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="66da7-108">Dirección de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para la colección de animaciones del carácter.</span><span class="sxs-lookup"><span data-stu-id="66da7-108">The address of the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the character's animation collection.</span></span>

</dd> </dl>

<span data-ttu-id="66da7-109">Esta función permite enumerar los nombres de las animaciones de un carácter.</span><span class="sxs-lookup"><span data-stu-id="66da7-109">This function enables you to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="66da7-110">Los elementos de la colección no tienen ninguna propiedad, por lo que no se puede tener acceso a los elementos individuales directamente.</span><span class="sxs-lookup"><span data-stu-id="66da7-110">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span> <span data-ttu-id="66da7-111">Para obtener acceso a la colección, consulte punkEnum para la interfaz IEnumVARIANT:</span><span class="sxs-lookup"><span data-stu-id="66da7-111">To access the collection, query punkEnum for the IEnumVARIANT interface:</span></span>


```c++
IEnumVARIANT pEnum;
VARIANT vAnimName;
DWORD dwRetrieved;

hRes = punkEnum->QueryInterface(IID_IEnumVARIANT, (LPVOID *)&pEnum);

if (SUCCEEDED(hRes)) {

    while (TRUE) {

         hRes = pEnum->Next(1, &vAnimName, &dwRetrieved);

         if (hRes != NOERROR)
            break;

         // vAnimName.bstrVal is the animation name

         VariantClear(&vAnimName);
    } 

    pEnum->Release();
}

punkEnum->Release();
```



> [!Note]  
> <span data-ttu-id="66da7-112">En el caso de los caracteres ACF, la colección devuelve todas las animaciones definidas para el carácter, agregando a las que se han recuperado con el método [**Get**](https://www.bing.com/search?q=**Get**) .</span><span class="sxs-lookup"><span data-stu-id="66da7-112">For ACF characters, the collection returns all the animations that have been defined for the character, adding to the ones that have been retrieved with the [**Get**](https://www.bing.com/search?q=**Get**) method.</span></span>
