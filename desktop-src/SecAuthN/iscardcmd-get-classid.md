---
description: Recupera el identificador de clase de la unidad de datos de protocolo de aplicación (APDU).
ms.assetid: 03ea997d-7698-43c7-aa9a-dfc1bac6fcdd
title: 'Método ISCardCmd:: get_ClassId (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6b78dfc9f3adf200a614b129ff1e86a16c88438f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154360"
---
# <a name="iscardcmdget_classid-method"></a>ISCardCmd:: get \_ ClassID (método)

\[El método **Get \_ ClassID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Get \_ ClassID** recupera el identificador de clase de la [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ClassId(
  [out] BYTE *pbyClass
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbyClass* \[ enuncia\]
</dt> <dd>

Puntero al byte que representa el identificador de clase.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pbyClass* no es válido.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *pbyClass*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                          |



 

## <a name="remarks"></a>Observaciones

Para establecer el identificador de clase en un nuevo valor, llame a [**Put \_ ClassID**](iscardcmd-put-classid.md).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardCmd**](iscardcmd.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo recuperar el identificador de clase. En el ejemplo se da por supuesto que pISCardCmd es un puntero válido a una instancia de la interfaz [**ISCardCmd**](iscardcmd.md) .


```C++
BYTE     byClassID;
HRESULT  hr;

// Retrieve the class ID.
hr = pISCardCmd->get_ClassId(&byClassID);
if (FAILED(hr))
{
  printf("Failed get_ClassId\n");
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

[**Put \_ ClassID**](iscardcmd-put-classid.md)
</dt> </dl>

 

 
