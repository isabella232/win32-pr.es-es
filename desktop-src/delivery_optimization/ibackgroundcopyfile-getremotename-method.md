---
title: Método IBackgroundCopyFile GetRemoteName (Deliveryoptimization.h)
description: Recupera el nombre remoto del archivo.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Método GetRemoteName
- Método GetRemoteName, interfaz IBackgroundCopyFile
- Interfaz IBackgroundCopyFile, método GetRemoteName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e84827f4c1144c4242f382aff822984b24dd83610c1ebd5d2540ba7c4ca65d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810339"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a>IBackgroundCopyFile::GetRemoteName (método)

Recupera el nombre remoto del archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppName* \[ out\]
</dt> <dd>

Cadena terminada en NULL que contiene el nombre remoto del archivo que se transferirá. El nombre es completo. Llame a [**la función CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppName* cuando haya terminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S_OK** correcto o uno de los valores **HRESULT COM** estándar en caso de error.

## <a name="remarks"></a>Comentarios

Para cambiar el nombre de archivo remoto, llame al [**método IBackgroundCopyFile2::SetRemoteName.**](ibackgroundcopyfile2-setremotename-method.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile se define como 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile::GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

