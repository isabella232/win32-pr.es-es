---
description: Determina el tamaño, en bytes, de la interfaz COM IStream.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'ISCardTypeConv:: SizeOfIStream (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648427"
---
# <a name="iscardtypeconvsizeofistream-method"></a>ISCardTypeConv:: SizeOfIStream (método)

\[El método **SizeOfIStream** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **SizeOfIStream** determina el tamaño, en bytes, de la interfaz com **IStream** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStrm* \[ de\]
</dt> <dd>

Puntero a la interfaz com **IStream** .

</dd> <dt>

*puliSize* \[ enuncia\]
</dt> <dd>

Puntero al entero grande sin signo que puede contener todo el valor de tamaño de bit 64 de la interfaz com **IStream** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | La función se ejecutó correctamente y *\* puliSize* es el tamaño, en bytes, de la interfaz com IStream.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Se produjo un error no especificado.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro *puliSize* es incorrecto.<br/>                                                       |
| <dl> <dt>**\_puntero E**</dt> </dl>    | El parámetro *pStrm* es incorrecto.<br/>                                                          |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Se ha producido un error inesperado.<br/>                                                                   |



 

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
| IID<br/>                      | IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valores devueltos de tarjeta inteligente](authentication-return-values.md)
</dt> </dl>

 

 
