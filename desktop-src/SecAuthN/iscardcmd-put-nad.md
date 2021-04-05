---
description: Especifica la dirección de nodo (NAD) que se va a usar con la interfaz ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: 'ISCardCmd: método de ut_Nad de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908298"
---
# <a name="iscardcmdput_nad-method"></a>ISCardCmd: \_ método Nad:p UT

\[El método **Put \_ nad** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método de **colocación del \_ nad** especifica la dirección del nodo (NAD) que se va a usar con la interfaz [**ISCardCmd**](iscardcmd.md) . Esto se aplica a las comunicaciones que usan solo las comunicaciones de [*Protocolo T = 1*](../secgloss/t-gly.md) . De forma predeterminada, el objeto [**ISCardCmd**](iscardcmd.md) usa un nad de cero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bNad* \[ de\]
</dt> <dd>

Byte que representa el NAD que se va a usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La operación se completó correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *bNad* no es válido.<br/>    |



 

## <a name="remarks"></a>Observaciones

Solo se debe llamar a este método cuando es necesario usar un valor distinto de cero para el nad.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo especificar la dirección de un nodo que se va a usar con la interfaz [**ISCardCmd**](iscardcmd.md) . En el ejemplo se da por supuesto que byNadValue es una variable de tipo **byte** a la que se asignó previamente un valor y que pISCardCmd es un puntero válido a una instancia de la interfaz **ISCardCmd** .


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
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
</dt> </dl>

 

 
