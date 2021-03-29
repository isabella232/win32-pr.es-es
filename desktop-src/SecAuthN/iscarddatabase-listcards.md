---
description: El método ListCards recupera todos los nombres de tarjetas inteligentes que coinciden con los identificadores de interfaz especificados (GUID), la cadena ATR especificada o ambos.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'ISCardDatabase:: ListCards (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e8a5bf56aa27a044d29e2e0153698bfefe69e1d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809913"
---
# <a name="iscarddatabaselistcards-method"></a>ISCardDatabase:: ListCards (método)

\[El método **ListCards** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **ListCards** recupera todos los nombres de tarjetas inteligentes que coinciden con los identificadores de interfaz especificados (GUID), la [*cadena ATR*](../secgloss/a-gly.md)especificada o ambos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAtr* \[ de\]
</dt> <dd>

Puntero a una cadena ATR de [*tarjeta inteligente*](../secgloss/s-gly.md) . La cadena ATR se debe empaquetar en un [**IByteBuffer**](ibytebuffer.md).

</dd> <dt>

*pInterfaceGuids* \[ de\]
</dt> <dd>

Puntero a una matriz SAFEARRAY de identificadores de interfaz COM (GUID) en formato BSTR.

</dd> <dt>

*localeId* \[ de\]
</dt> <dd>

Identificador de localización de idioma.

</dd> <dt>

*ppCardNames* \[ enuncia\]
</dt> <dd>

Puntero a un SAFEARRAY de BSTR que contiene los nombres de las tarjetas inteligentes que cumplen los parámetros de búsqueda si se realizan correctamente; **Null** si se produjo un error en la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Observaciones

Para recuperar todos los [*lectores o lectores*](../secgloss/r-gly.md) [*conocidos, llame*](../secgloss/r-gly.md)a [**ListReaders**](iscarddatabase-listreaders.md) o [**ListReaderGroups**](iscarddatabase-listreadergroups.md) , respectivamente.

Para recuperar el [*servicio principal*](../secgloss/p-gly.md) o las interfaces de una tarjeta específica [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) o [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivamente.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardDatabase**](iscarddatabase.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar los nombres de las tarjetas inteligentes que coinciden con la cadena ATR especificada.


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardDatabase se define como 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetProviderCardId**](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[**ISCardDatabase**](iscarddatabase.md)
</dt> <dt>

[**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[**ListReaderGroups**](iscarddatabase-listreadergroups.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
