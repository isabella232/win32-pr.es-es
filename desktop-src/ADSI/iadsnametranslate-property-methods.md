---
title: Métodos de propiedad IADsNameTranslate (Iads.h)
description: Establece la propiedad ChaseReferral.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- IADsNameTranslate Property Methods ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3993c3f3680dca46d2f880705fae44812a3bb5fd7a046084c1d818c3433ea7f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082389"
---
# <a name="iadsnametranslate-property-methods"></a>Métodos de propiedad IADsNameTranslate

El método de propiedad [**de la interfaz IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) establece la **propiedad ChaseReferral.** Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**ChaseReferral**
</dt> <dd> <dl>

Opciones de búsqueda de referencias, tal como se define en [**\_ ADS CHASE \_ REFERRALS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum). Cuando se establece la búsqueda de referencias, la traducción de nombres se realiza en objetos que no pertenecen a este directorio y son las referencias devueltas de la búsqueda de referencias.

<dt>

Tipo de acceso: solo escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentarios

Las opciones de búsqueda de referencias solo se aplican cuando se usan [**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) e [**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get). La característica no está disponible con [**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) o [**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).

La [**interfaz IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) tiene una implementación parcial de [**ADS CHASE \_ \_ REFERRALS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) mediante la **propiedad ChaseReferral.** Si la **propiedad ChaseReferral** se establece en cero (0), es lo mismo que especificar **ADS CHASE \_ \_ REFERRALS \_ NEVER** (0). Si se usa un valor distinto de cero, es lo mismo que especificar **ADS \_ CHASE \_ REFERRALS \_ ALWAYS** (0x60). **IADsNameTranslate** no implementa las opciones **ADS \_ CHASE \_ REFERRALS \_ SUBORDINATE** (0x20) o **ADS CHASE \_ \_ REFERRALS \_ EXTERNAL** (0x40).

La configuración predeterminada para la búsqueda de referencias está habilitada **(ADS \_ CHASE \_ REFERRALS \_ ALWAYS**). Sin la búsqueda de referencias, puede realizar la traducción de nombres en los objetos que residen solo en el servidor de directorio conectado. Si no está seguro de si el objeto de interés está en el servidor especificado, debe establecer esta propiedad en **ADS \_ CHASE \_ REFERRALS \_ ALWAYS**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNameTranslate se define como B1B272A3-3625-11D1-A3A4-00C04FB950DC<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ENUMERACIÓN \_ DE REFERENCIAS DE ADS \_ CHASE \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[**IADsNameTranslate::Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[**IADsNameTranslate::Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

 





