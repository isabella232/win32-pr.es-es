---
description: Revise el texto del proveedor de forma más exhaustiva que ISpellCheckProvider::Check.
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: IComprehensiveSpellCheckProvider::ComprehensiveCheck (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: ee1b07eb2f459aca3955b0a1c5ad2e2e2139cc196f618430b3039b1eba1e3971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086605"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>IComprehensiveSpellCheckProvider::ComprehensiveCheck (método)

Revise el texto del proveedor de forma más exhaustiva que [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*text* \[ En\]
</dt> <dd>

Texto que se comprobará.

</dd> <dt>

*resultado* \[ out\]
</dt> <dd>

Resultado de comprobar este texto, como una enumeración de errores ortográficos ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), si los hay.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor devuelto                                                                             | Descripción                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>S \_ OK</dt> </dl>         | Exitoso.<br/>                |
| <dl> <dt>E \_ INVALIDARG</dt> </dl> | *text* es una cadena vacía.<br/> |
| <dl> <dt>PUNTERO \_ E</dt> </dl>    | *text* es un puntero nulo.<br/>  |



 

## <a name="remarks"></a>Comentarios

No es necesario que un proveedor de revisión ortórque implemente esta interfaz. Pero si el proveedor admite dos "modos" de revisión ortográfica (uno más rápido y uno más lento pero más exhaustivo), debe implementar esta interfaz en el mismo objeto que implementa [**ISpellCheckProvider para**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) admitir el modo de comprobación más exhaustivo. Cuando un cliente llama a [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), la funcionalidad de revisión ortográfica [**consultará al**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) proveedor para [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)y llamará a **IComprehensiveSpellCheckProvider.ComprehensiveCheck si** se admite la interfaz. Si no se admite la interfaz, volverá a [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)de forma silenciosa.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
