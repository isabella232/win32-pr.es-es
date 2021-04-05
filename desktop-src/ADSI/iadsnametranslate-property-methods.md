---
title: Métodos de la propiedad IADsNameTranslate (iAds. h)
description: Establece la propiedad ChaseReferral.
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsNameTranslate ADSI
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
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996831"
---
# <a name="iadsnametranslate-property-methods"></a>Métodos de propiedad IADsNameTranslate

El método Property de la interfaz [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) establece la propiedad **ChaseReferral** . Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**ChaseReferral**
</dt> <dd> <dl>

Opciones de seguimiento de referencia tal y como se define en la [**\_ \_ \_ enumeración**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)de referencias de seguimiento de anuncios. Cuando se establece el seguimiento de referencias, la traducción del nombre se realiza en objetos que no pertenecen a este directorio y son las referencias devueltas por el seguimiento de la referencia.

<dt>

Tipo de acceso: solo escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Observaciones

Las opciones de seguimiento de referencia solo se aplican cuando se usa [**IADsNameTranslate:: set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) y [**IADsNameTranslate:: get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get). La característica no está disponible con [**IADsNameTranslate:: SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex) o [**IADsNameTranslate:: GETEX**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex).

La interfaz [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) tiene una implementación parcial de [**la \_ \_ \_ enumeración de referencias de seguimiento de anuncios**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) mediante la propiedad **ChaseReferral** . Si la propiedad **ChaseReferral** se establece en cero (0), es lo mismo que especificar las **referencias de \_ seguimiento de anuncios \_ \_ nunca** (0). Si se usa un valor distinto de cero, es lo mismo que especificar las **referencias de seguimiento de anuncios \_ \_ \_ siempre** (0x60). **IADsNameTranslate** no implementa las opciones externas de referencias de **\_ seguimiento \_ \_ subordinadas** (0X20) **o \_ \_ referencias \_ de seguimiento de ADS** (0x40).

La configuración predeterminada para el seguimiento de referencias está habilitada (las **referencias de seguimiento de anuncios \_ \_ \_ siempre**). Sin el seguimiento de la referencia, puede hacer que la traducción del nombre se realice en los objetos que residen solo en el servidor de directorio conectado. Si no está seguro de si el objeto de interés está en el servidor especificado, debe establecer esta propiedad para que sea **\_ \_ \_ siempre referencias de seguimiento de anuncios**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNameTranslate se define como B1B272A3-3625-11D1-A3A4-00C04FB950DC<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_ \_ enumeración de referencias de seguimiento de ADS \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[**IADsNameTranslate:: get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[**IADsNameTranslate:: set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

 





