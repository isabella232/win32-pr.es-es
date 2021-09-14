---
description: Compruebe el texto del proveedor de forma más exhaustiva que ISpellCheckProvider::Check.
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: IComprehensiveSpellCheckProvider::ComprehensiveCheck (Método)
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
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274596"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>IComprehensiveSpellCheckProvider::ComprehensiveCheck (Método)

Compruebe el texto del proveedor de forma más exhaustiva que [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

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



 

## <a name="remarks"></a>Observaciones

Esta interfaz no es necesaria para que la implemente un proveedor de spell check. Pero si el proveedor admite dos "modos" de revisión ortográfica (uno más rápido y uno más lento pero más exhaustivo), debe implementar esta interfaz en el mismo objeto que implementa [**ISpellCheckProvider para**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) admitir el modo de comprobación más exhaustivo. Cuando un cliente llama a [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), la funcionalidad de corrector ortográfico [**consultará al**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) proveedor de [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)y llamará a **IComprehensiveSpellCheckProvider.ComprehensiveCheck si** se admite la interfaz. Si no se admite la interfaz, volverá a [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)de forma silenciosa.

## <a name="see-also"></a>Consulte también

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

 

 
