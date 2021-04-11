---
description: El método ListReaderGroups recupera los nombres de los grupos de lectores registrados en la base de datos de tarjeta inteligente.
ms.assetid: 81f6356a-92eb-4d27-abfe-e4a32de14d1c
title: 'ISCardDatabase:: ListReaderGroups (método) (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListReaderGroups
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 00753b0ca3964dc5a35e26db0eec2aedda4d2511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154350"
---
# <a name="iscarddatabaselistreadergroups-method"></a>ISCardDatabase:: ListReaderGroups (método)

\[El método **ListReaderGroups** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **ListReaderGroups** recupera los nombres de los [*grupos de lectores*](../secgloss/r-gly.md) registrados en la base de datos de tarjeta inteligente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ListReaderGroups(
  [in]  LONG        localeId,
  [out] LPSAFEARRAY *ppReaderGroups
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*localeId* \[ de\]
</dt> <dd>

IDENTIFICADOR de localización de idioma.

</dd> <dt>

*ppReaderGroups* \[ enuncia\]
</dt> <dd>

Puntero a un SAFEARRAY de BSTR que contiene los nombres de los grupos de lectores de tarjetas inteligentes que cumplen los parámetros de búsqueda si se realizan correctamente; **Null** si se produjo un error en la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                            |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *ppReaderGroups*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                                |



 

## <a name="remarks"></a>Observaciones

Para recuperar todas las [*tarjetas inteligentes*](../secgloss/s-gly.md) o [*lectores*](../secgloss/r-gly.md)conocidos, llame a [**ListCards**](iscarddatabase-listcards.md) o [**ListReaders**](iscarddatabase-listreaders.md) , respectivamente.

Para recuperar el [*proveedor de servicios principal*](../secgloss/p-gly.md) o las interfaces de una tarjeta específica [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) o [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) , respectivamente.

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardDatabase**](iscarddatabase.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar los nombres de los grupos de lectores registrados en la base de datos de tarjeta inteligente.


```C++
LPSAFEARRAY pGroups = NULL;
HRESULT     hr;

// Determine the reader groups.
hr = pISCDataBase->ListReaderGroups(0x0409,  // English (US)
                                    &pGroups);
if (FAILED(hr))
{
   printf("Failed ListReaderGroups\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
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

[**ListCards**](iscarddatabase-listcards.md)
</dt> <dt>

[**ListReaders**](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
