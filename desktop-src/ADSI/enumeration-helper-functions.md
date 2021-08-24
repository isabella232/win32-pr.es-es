---
title: Funciones auxiliares de enumeración
description: Hay tres funciones auxiliares de enumerador que se pueden usar desde C/C++ para ayudar en la navegación de Active Directory objetos. Son ADsBuildEnumerator, ADsEnumerateNext y ADsFreeEnumerator.
ms.assetid: 019958c8-5bf5-45eb-871c-796ff3750cdc
ms.tgt_platform: multiple
keywords:
- ADsBuildEnumerator ADSI ,using
- ADsEnumerateNext ADSI ,using
- ADsFreeEnumerator ADSI ,using
- ADSI ADSI , código de ejemplo C/C++ , mediante ADsBuildEnumerator ADsEnumerateNext y ADsFreeEnumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c110fbc4fddd420bf8205d6c2d894c7d4f4daf8287312c2d0d86002f5520310b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082659"
---
# <a name="enumeration-helper-functions"></a>Funciones auxiliares de enumeración

Hay tres funciones auxiliares de enumerador que se pueden usar desde C/C++ para ayudar en la navegación de Active Directory objetos. Son [**ADsBuildEnumerator,**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)y [**ADsFreeEnumerator.**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)

## <a name="adsbuildenumerator"></a>ADsBuildEnumerator

La [**función auxiliar ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) encapsula el código necesario para crear un objeto enumerador. Llama al método [**IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) para crear un objeto enumerador y, a continuación, llama al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para obtener un puntero a la [**interfaz IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) para ese objeto. El objeto de enumeración es el mecanismo de Automation para enumerar sobre contenedores. Use la [**función ADsFreeEnumerator para**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) liberar este objeto enumerador.

## <a name="adsenumeratenext"></a>ADsEnumerateNext

La [**función auxiliar ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) rellena una matriz VARIANT con elementos obtenidos de un objeto enumerador. El número de elementos recuperados puede ser menor que el número solicitado.

## <a name="adsfreeenumerator"></a>ADsFreeEnumerator

Libera un objeto enumerador creado anteriormente a través de [**la función ADsBuildEnumerator.**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)

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



 

 