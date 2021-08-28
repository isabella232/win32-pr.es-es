---
description: El método GetProviderCardId recupera el identificador (GUID) del proveedor de servicios principal para la tarjeta inteligente especificada.
ms.assetid: 0008bb5a-872f-4e5d-9029-a863cd3eea00
title: Método ISCardDatabase::GetProviderCardId (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.GetProviderCardId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 814eec89f8ff92d81dd911101d79e516500f0baeb363dd4148bd466de849bc24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577285"
---
# <a name="iscarddatabasegetprovidercardid-method"></a>Método ISCardDatabase::GetProviderCardId

\[El **método GetProviderCardId** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método GetProviderCardId** recupera el identificador (GUID) del proveedor [*de servicios principal*](../secgloss/p-gly.md) para la tarjeta inteligente [*especificada.*](../secgloss/s-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetProviderCardId(
  [in]  BSTR   bstrCardName,
  [out] LPGUID *ppguidProviderId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrCardName* \[ En\]
</dt> <dd>

Nombre de la tarjeta inteligente.

</dd> <dt>

*ppguidProviderId* \[ out\]
</dt> <dd>

Puntero al identificador (GUID) del proveedor de servicios principal si se realiza correctamente; **NULL si** no se pudo hacer la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                              |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido *en ppguidProviderId.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                                  |



 

## <a name="remarks"></a>Comentarios

Para enumerar las interfaces de la tarjeta inteligente, llame [**a ListCardInterfaces**](iscarddatabase-listcardinterfaces.md).

Para recuperar todas las [](../secgloss/r-gly.md) tarjetas [*inteligentes conocidas,*](../secgloss/s-gly.md)los lectores y los grupos de lectores llaman a [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)y [**ListReaderGroups,**](iscarddatabase-listreadergroups.md) respectivamente. [](../secgloss/r-gly.md)

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardDatabase**](iscarddatabase.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar el identificador del proveedor de servicios principal para la tarjeta inteligente especificada.


```C++
BSTR     bstrCard = NULL;
LPGUID   pguidProvId = NULL;
HRESULT  hr;

bstrCard = SysAllocString(L"My Card");
hr = pISCDataBase->GetProviderCardId(bstrCard,&pguidProvId);
if (FAILED(hr))
{
   printf("Failed GetProviderCardId\n");
}
else
{
    // Use pguidProvId as needed.
}

// Free BSTR when done.
if ( NULL != bstrCard )
{
    SysFreeString(bstrCard);
    bstrCard=NULL;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardDatabase se define como 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
