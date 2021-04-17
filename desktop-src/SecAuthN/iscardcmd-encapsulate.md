---
description: El método Encapsulate encapsula la unidad de datos de protocolo de aplicación de comandos (APDU) determinada en otra APDU de comando para su transmisión a una tarjeta inteligente.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: 'ISCardCmd:: Encapsulate (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cd671a11edd9977695eeaf858e38f962b3dd0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652917"
---
# <a name="iscardcmdencapsulate-method"></a>ISCardCmd:: Encapsulate (método)

\[El método **Encapsulate** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Encapsulate** encapsula la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) de comandos (APDU) determinada en otra APDU de comando para su transmisión a una [*tarjeta inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pApdu* \[ de\]
</dt> <dd>

Puntero a la APDU que se va a encapsular.

</dd> <dt>

*ApduType* \[ de\]
</dt> <dd>

ISO 7816-4 Case for [*T = 0*](../secgloss/t-gly.md) transmisiones.

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

**\_Caso ISO \_ 1**
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

**\_Caso ISO \_ 2**
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

**\_Caso \_ 3 de ISO**
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

**ISO \_ Case \_ 4**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parámetro no válido.<br/>                   |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *pApdu*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                       |



 

## <a name="remarks"></a>Observaciones

Para compilar una APDU de comando, llame a [**BuildCmd**](iscardcmd-buildcmd.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo encapsular una APDU de comando. En el ejemplo se da por supuesto que pIByteApdu es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) .


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
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

[**BuildCmd**](iscardcmd-buildcmd.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
