---
title: Funciones auxiliares de enumeración
description: Hay tres funciones auxiliares de enumerador que se pueden usar desde C/C++ para ayudar en la navegación de objetos de Active Directory. Son ADsBuildEnumerator, ADsEnumerateNext y ADsFreeEnumerator.
ms.assetid: 019958c8-5bf5-45eb-871c-796ff3750cdc
ms.tgt_platform: multiple
keywords:
- ADsBuildEnumerator ADSI, usar
- ADsEnumerateNext ADSI, usar
- ADsFreeEnumerator ADSI, usar
- ADSI ADSI, código de ejemplo C/C++, uso de ADsBuildEnumerator ADsEnumerateNext y ADsFreeEnumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9597787202adf183435262eab9341957e19457
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149622"
---
# <a name="enumeration-helper-functions"></a><span data-ttu-id="81ce2-108">Funciones auxiliares de enumeración</span><span class="sxs-lookup"><span data-stu-id="81ce2-108">Enumeration Helper Functions</span></span>

<span data-ttu-id="81ce2-109">Hay tres funciones auxiliares de enumerador que se pueden usar desde C/C++ para ayudar en la navegación de objetos de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="81ce2-109">There are three enumerator helper functions that can be used from C/C++ to aid in the navigation of Active Directory objects.</span></span> <span data-ttu-id="81ce2-110">Son [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)y [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span><span class="sxs-lookup"><span data-stu-id="81ce2-110">They are [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext), and [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span></span>

## <a name="adsbuildenumerator"></a><span data-ttu-id="81ce2-111">ADsBuildEnumerator</span><span class="sxs-lookup"><span data-stu-id="81ce2-111">ADsBuildEnumerator</span></span>

<span data-ttu-id="81ce2-112">La función auxiliar [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) encapsula el código necesario para crear un objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="81ce2-112">The [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) helper function encapsulates the code required to create an enumerator object.</span></span> <span data-ttu-id="81ce2-113">Llama al método [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) para crear un objeto de enumerador y, a continuación, llama al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para obtener un puntero a la interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) para ese objeto.</span><span class="sxs-lookup"><span data-stu-id="81ce2-113">It calls the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) method to create an enumerator object and then calls the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to get a pointer to the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface for that object.</span></span> <span data-ttu-id="81ce2-114">El objeto de enumeración es el mecanismo de automatización que se va a enumerar en contenedores.</span><span class="sxs-lookup"><span data-stu-id="81ce2-114">The enumeration object is the Automation mechanism to enumerate over containers.</span></span> <span data-ttu-id="81ce2-115">Utilice la función [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) para liberar este objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="81ce2-115">Use the [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) function to release this enumerator object.</span></span>

## <a name="adsenumeratenext"></a><span data-ttu-id="81ce2-116">ADsEnumerateNext</span><span class="sxs-lookup"><span data-stu-id="81ce2-116">ADsEnumerateNext</span></span>

<span data-ttu-id="81ce2-117">La función auxiliar [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) rellena una matriz de variantes con elementos capturados de un objeto de enumerador.</span><span class="sxs-lookup"><span data-stu-id="81ce2-117">The [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) helper function populates a VARIANT array with elements fetched from an enumerator object.</span></span> <span data-ttu-id="81ce2-118">El número de elementos recuperados puede ser menor que el número solicitado.</span><span class="sxs-lookup"><span data-stu-id="81ce2-118">The number of elements retrieved can be smaller than the number requested.</span></span>

## <a name="adsfreeenumerator"></a><span data-ttu-id="81ce2-119">ADsFreeEnumerator</span><span class="sxs-lookup"><span data-stu-id="81ce2-119">ADsFreeEnumerator</span></span>

<span data-ttu-id="81ce2-120">Libera un objeto de enumerador creado previamente a través de la función [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) .</span><span class="sxs-lookup"><span data-stu-id="81ce2-120">Frees an enumerator object previously created through the [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) function.</span></span>

<span data-ttu-id="81ce2-121">En el ejemplo de código siguiente se muestra una función que usa funciones auxiliares de enumerador en C++.</span><span class="sxs-lookup"><span data-stu-id="81ce2-121">The following code example shows a function that uses enumerator helper functions in C++.</span></span>


```C++
/*****************************************************************************
  Function:    TestEnumObject
  Arguments:   pszADsPath - ADsPath of the container to be enumerated (WCHAR*).
  Return:      S_OK if successful, an error code otherwise.
  Purpose:     Example using ADsBuildEnumerator, ADsEnumerateNext and
               ADsFreeEnumerator.
******************************************************************************/
#define MAX_ENUM      100  
 
HRESULT
TestEnumObject( LPWSTR pszADsPath )
{
    ULONG cElementFetched = 0L;
    IEnumVARIANT * pEnumVariant = NULL;
    VARIANT VariantArray[MAX_ENUM];
    HRESULT hr = S_OK;
    IADsContainer * pADsContainer =  NULL;
    DWORD dwObjects = 0, dwEnumCount = 0, i = 0;
    BOOL  fContinue = TRUE;
 
 
    hr = ADsGetObject(
                pszADsPath,
                IID_IADsContainer,
                (void **)&pADsContainer
                );
 
 
    if (FAILED(hr)) {
 
        printf("\"%S\" is not a valid container object.\n", pszADsPath) ;
        goto exitpoint ;
    }
 
    hr = ADsBuildEnumerator(
            pADsContainer,
            &pEnumVariant
            );
 
    if( FAILED( hr ) )
    {
      printf("ADsBuildEnumerator failed with %lx\n", hr ) ;
      goto exitpoint ;
    }
 
    fContinue  = TRUE;
    while (fContinue) {
 
        IADs *pObject ;
 
        hr = ADsEnumerateNext(
                    pEnumVariant,
                    MAX_ENUM,
                    VariantArray,
                    &cElementFetched
                    );

        if ( FAILED( hr ) )
        {
            printf("ADsEnumerateNext failed with %lx\n",hr);
            goto exitpoint;
        }
 
        if (hr == S_FALSE) {
            fContinue = FALSE;
        }
 
        dwEnumCount++;
 
        for (i = 0; i < cElementFetched; i++ ) {
 
            IDispatch *pDispatch    = NULL;
            BSTR        bstrADsPath = NULL;
 
            pDispatch = VariantArray[i].pdispVal;
 
            hr = V_DISPATCH( VariantArray + i )->QueryInterface(IID_IADs, (void **) &pObject) ;
 
            if( SUCCEEDED( hr ) )
            {
               pObject->get_ADsPath( &bstrADsPath );
               printf( "%S\n", bstrADsPath );
            }
            pObject->Release();
            VariantClear( VariantArray + i );
            SysFreeString( bstrADsPath );
        }
 
        dwObjects += cElementFetched;
    }
 
    printf("Total Number of Objects enumerated is %d\n", dwObjects);
 
exitpoint:
    if (pEnumVariant) {
        ADsFreeEnumerator( pEnumVariant );
    }
 
    if (pADsContainer) {
        pADsContainer->Release();
    }
 
    return(hr);
}
```



 

 