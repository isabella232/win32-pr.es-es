---
description: Recupera el valor del identificador de clase alternativo.
ms.assetid: 80c7cbba-e28d-4973-9f3f-7636ff331b64
title: 'Método ISCardCmd:: get_AlternateClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8cfc47011881ae3e3f6df5ef51c910899a054f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649179"
---
# <a name="iscardcmdget_alternateclassid-method"></a>ISCardCmd:: get \_ AlternateClassId (método)

\[El método **Get \_ AlternateClassId** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Get \_ AlternateClassId** recupera el valor del identificador de clase alternativo. Este método producirá un error a menos que se haya establecido el identificador alternativo mediante una llamada anterior a [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AlternateClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbyClass* \[ enuncia\]
</dt> <dd>

Puntero al byte que contiene el valor de identificador de clase alternativo en la devolución.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve los siguientes valores posibles.



| Código devuelto                                                                                    | Descripción                                                                                                                                 |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>           | La operación se completó correctamente.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | El parámetro *pbyClass* no es válido.<br/>                                                                                           |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | El identificador de clase alternativo no se ha establecido previamente mediante una llamada a [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).<br/> |



 

## <a name="remarks"></a>Observaciones

Este método se aplica a las comunicaciones que usan el [*Protocolo T = 0*](../secgloss/t-gly.md). Para obtener más información, consulte [**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar el identificador de clase alternativo. En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE     byAltClassID;
HRESULT  hr;

// Retrieve the alternate class ID.
hr = pISCardCmd->get_AlternateClassId(&byAltClassID);
if (FAILED(hr))
{
  printf("Failed get_AltClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**Put \_ AlternateClassId**](iscardcmd-put-alternateclassid.md)
</dt> </dl>

 

 
