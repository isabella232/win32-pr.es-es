---
description: Establece el campo de datos en la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: 'ISCardCmd: método de ut_Data de:p (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155105"
---
# <a name="iscardcmdput_data-method"></a>ISCardCmd::p \_ método de datos UT

\[El método **Put \_ Data** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Put \_ Data** establece el campo de datos en la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdata* \[ de\]
</dt> <dd>

Puntero al objeto de búfer de bytes (**IStream**) que se va a copiar en el campo de datos APDU.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pdata* no es válido.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero incorrecto en *pdata*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                       |



 

## <a name="remarks"></a>Observaciones

Cuando se establece una nueva parte de datos del mensaje, la longitud del campo de datos se calcula y se almacena en el parámetro P3 de la APDU. Para recuperar la longitud del campo de datos, llame a [**Get \_ P3**](iscardcmd-get-p3.md).

Para recuperar el campo de datos de APDU, llame a [**Get \_ Data**](iscardcmd-get-data.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer el campo de datos en la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU). En el ejemplo se da por supuesto que pIByteData es un puntero válido a una instancia de la interfaz [**IByteBuffer**](ibytebuffer.md) y que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
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

[**obtener \_ datos**](iscardcmd-get-data.md)
</dt> <dt>

[**obtener \_ P3**](iscardcmd-get-p3.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
