---
title: Método INapComponentInfo GetIcon (NapCommon. h)
description: Lo usa el sistema NAP para obtener el icono de un cliente de mantenimiento.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- Método GetIcon NAP
- Método GetIcon NAP, interfaz INapComponentInfo
- Interfaz INapComponentInfo NAP, método GetIcon
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997007"
---
# <a name="inapcomponentinfogeticon-method"></a>INapComponentInfo:: GetIcon (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El sistema NAP usa el método de devolución de llamada **INapComponentInfo:: GetIcon** para obtener el icono de un cliente de mantenimiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dllFilePath* \[ enuncia\]
</dt> <dd>

Un puntero a un puntero a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) usado para devolver la ruta de acceso del archivo DLL que contiene el icono.

</dd> <dt>

*iconResourceId* \[ enuncia\]
</dt> <dd>

Puntero al valor que se usa para devolver el identificador de recurso del icono que se va a usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva uno de estos códigos de error en función del resultado de esta operación.



| Código devuelto                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> </dl>           | La operación se realizó correctamente.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Error de permisos, acceso denegado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Límite de recursos del sistema, no se pudo realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Los iconos deben localizarse según el identificador de idioma del subproceso que realiza la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





