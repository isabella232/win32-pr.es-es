---
description: Especifica la dirección del nodo (Nad) que se va a usar con la interfaz ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: Método ISCardCmd::p ut_Nad (Scarddat.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160979"
---
# <a name="iscardcmdput_nad-method"></a>Método ISCardCmd::p ut \_ Nad

\[El **método put \_ Nad** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método put \_ Nad** especifica la dirección del nodo (Nad) que se va a usar con la [**interfaz ISCardCmd.**](iscardcmd.md) Esto se aplica solo a las comunicaciones que usan las comunicaciones del [*protocolo T=1.*](../secgloss/t-gly.md) De forma predeterminada, [**el objeto ISCardCmd**](iscardcmd.md) usa un Objeto Nad de cero.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bNad* \[ En\]
</dt> <dd>

Byte que representa el objeto Nad que se usará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | La operación se completó correctamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro bNad* no es válido.<br/>    |



 

## <a name="remarks"></a>Observaciones

Solo se debe llamar a este método cuando sea necesario usar un valor distinto de cero para el .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo especificar una dirección de nodo que se usará con la [**interfaz ISCardCmd.**](iscardcmd.md) En el ejemplo se supone que byNadValue es una variable de tipo **BYTE** a la que se asignó previamente un valor y que pISCardCmd es un puntero válido a una instancia de la interfaz **ISCardCmd.**


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
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd se define como \_ D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
