---
description: 'Revise el texto del proveedor de forma más exhaustiva que ISpellCheckProvider:: check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'IComprehensiveSpellCheckProvider:: ComprehensiveCheck (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688709"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>IComprehensiveSpellCheckProvider:: ComprehensiveCheck (método)

Revise el texto del proveedor de forma más exhaustiva que [**ISpellCheckProvider:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*texto* \[ de de\]
</dt> <dd>

Texto que se va a comprobar.

</dd> <dt>

*resultado* \[ de enuncia\]
</dt> <dd>

Resultado de la comprobación de este texto, como una enumeración de errores ortográficos ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), si existe.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor devuelto                                                                             | Descripción                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>S \_ correcto</dt> </dl>         | Ejecutado.<br/>                |
| <dl> <dt>E \_ INVALIDARG</dt> </dl> | el *texto* es una cadena vacía.<br/> |
| <dl> <dt>\_puntero E</dt> </dl>    | el *texto* es un puntero nulo.<br/>  |



 

## <a name="remarks"></a>Observaciones

No es necesario que la interfaz la implemente un proveedor de revisión ortográfica. Pero si el proveedor admite dos "modos" de revisión ortográfica (más rápido y más lento, pero más exhaustivo), debe implementar esta interfaz en el mismo objeto que implementa [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) para admitir el modo de comprobación más exhaustivo. Cuando un cliente llama a [**elemento:: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), la funcionalidad de revisión ortográfica ejecutará [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el proveedor de [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)y llamará a **IComprehensiveSpellCheckProvider. ComprehensiveCheck** si se admite la interfaz. Si no se admite la interfaz, se revertirá a [**ISpellCheckProvider:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[**Elemento:: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[**ISpellCheckProvider:: check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
