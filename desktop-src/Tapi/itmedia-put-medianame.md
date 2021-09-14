---
description: El método put \_ MediaName establece el nombre del medio. Los medios definidos son audio, vídeo, pizarra, texto y datos.
ms.assetid: 0dd18add-6c7e-40a8-8b39-10c65bdfb2e0
title: ItMedia::p ut_MediaName (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dcbd4e29f59694d610fb4e6af9fd49aa53323d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250268"
---
# <a name="itmediaput_medianame-method"></a>ItMedia::p ut \_ MediaName (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método put \_ MediaName** establece el nombre del medio. Los medios definidos son audio, vídeo, pizarra, texto y datos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MediaName(
  [in] BSTR pMediaName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMediaName* \[ En\]
</dt> <dd>

Puntero a un **BSTR** que contiene el nombre de medio que se va a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pMediaName* no es un puntero válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysAllocString para**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) asignar memoria para el parámetro *pMediaName* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria cuando la variable ya no sea necesaria.

Esta función puede enviar datos a través de la conexión sin cifrar; por lo tanto, alguien que intercepta en la red puede leer los datos. El riesgo de seguridad de enviar los datos en texto sin formato debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::get \_ MediaName**](itmedia-get-medianame.md)
</dt> </dl>

 

