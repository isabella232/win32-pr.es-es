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
# <a name="enumeration-helper-functions"></a>Funciones auxiliares de enumeración

Hay tres funciones auxiliares de enumerador que se pueden usar desde C/C++ para ayudar en la navegación de objetos de Active Directory. Son [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)y [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).

## <a name="adsbuildenumerator"></a>ADsBuildEnumerator

La función auxiliar [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) encapsula el código necesario para crear un objeto de enumerador. Llama al método [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) para crear un objeto de enumerador y, a continuación, llama al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para obtener un puntero a la interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) para ese objeto. El objeto de enumeración es el mecanismo de automatización que se va a enumerar en contenedores. Utilice la función [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) para liberar este objeto de enumerador.

## <a name="adsenumeratenext"></a>ADsEnumerateNext

La función auxiliar [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) rellena una matriz de variantes con elementos capturados de un objeto de enumerador. El número de elementos recuperados puede ser menor que el número solicitado.

## <a name="adsfreeenumerator"></a>ADsFreeEnumerator

Libera un objeto de enumerador creado previamente a través de la función [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) .

En el ejemplo de código siguiente se muestra una función que usa funciones auxiliares de enumerador en C++.


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



 

 