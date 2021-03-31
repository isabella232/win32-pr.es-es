---
title: Método IBackgroundCopyFile GetLocalName (Deliveryoptimization. h)
description: Recupera el nombre local del archivo.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- Método GetLocalName
- Método GetLocalName, interfaz IBackgroundCopyFile
- Interfaz IBackgroundCopyFile, método GetLocalName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079287"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a>IBackgroundCopyFile:: GetLocalName (método)

Recupera el nombre local del archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppName* \[ enuncia\]
</dt> <dd>

Cadena terminada en null que contiene el nombre del archivo en el cliente. El nombre es completo. Llame a la función [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppName* cuando termine.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.

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

[**IBackgroundCopyFile::GetRemoteName**](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

