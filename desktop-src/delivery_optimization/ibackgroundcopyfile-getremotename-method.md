---
title: Método IBackgroundCopyFile GetRemoteName (Deliveryoptimization. h)
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
ms.openlocfilehash: 9984ed9971fdfb91279dabc5810490b62804b7e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079285"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a>IBackgroundCopyFile:: GetRemoteName (método)

Recupera el nombre remoto del archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppName* \[ enuncia\]
</dt> <dd>

Cadena terminada en null que contiene el nombre remoto del archivo que se va a transferir. El nombre es completo. Llame a la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppName* cuando termine.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.

## <a name="remarks"></a>Observaciones

Para cambiar el nombre del archivo remoto, llame al método [**IBackgroundCopyFile2:: SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile se define como 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile::GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

