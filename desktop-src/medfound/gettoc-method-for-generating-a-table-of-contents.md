---
description: Función GetToc para generar una tabla de contenido
ms.assetid: f2f312ff-3519-4269-8252-eb52d2bc2e56
title: Función GetToc para generar una tabla de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b24da42f39ba5a499492bac8a166ffcfa883aab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474271"
---
# <a name="gettoc-function-for-generating-a-table-of-contents"></a>Función GetToc para generar una tabla de contenido

La siguiente función es una función auxiliar de un programa de ejemplo que se describe en Generar automáticamente una [tabla de contenido.](generating-a-table-of-contents-automatically.md)


```C++
HRESULT GetToc(IDMOWrapperFilter* pWrap, IToc** ppToc)
{
   IPropertyStore* pStore = NULL;
   HRESULT  hr = pWrap->QueryInterface(IID_IPropertyStore, (VOID**)&pStore);

   if(SUCCEEDED(hr))
   {
      PROPVARIANT pv;
      PropVariantInit(&pv);

      pv.vt = VT_BOOL;
      pv.bVal = VARIANT_TRUE;                                                     
      hr = pStore->SetValue(MFPKEY_TOCGENERATOR_ENDSIGNAL, pv);

      if(SUCCEEDED(hr))
      {
         for(LONG j = 0; j < 10; ++j)
         {
            PropVariantClear(&pv);
            pv.vt = VT_BOOL;
            hr = pStore->GetValue(MFPKEY_TOCGENERATOR_TOCREADY, &pv);

            if(SUCCEEDED(hr) && 1 == pv.bVal)  // Note: 1 is not equal to VARIANT_TRUE.
            {
               PropVariantClear(&pv);
               pv.vt = VT_UNKNOWN;
               hr = pStore->GetValue(MFPKEY_TOCGENERATOR_TOCOBJECT, &pv);

               if(SUCCEEDED(hr))
               {
                  *ppToc = (IToc*)pv.punkVal;
               }

               break;
            }

            Sleep(200);
            hr = ERROR_TIMEOUT;       
         }
      }

      pStore->Release();
      pStore = NULL;
   }
   
   return hr;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Generar automáticamente una tabla de contenido](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



