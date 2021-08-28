---
description: El método get \_ Invert recupera un valor booleano que indica si se invierte la operación de clave. Esta propiedad se aplica a todos los tipos de clave excepto DXTKEY \_ ALPHA.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: Método IDxtKey::get_Invert (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c5a862e062175d3c052a5003a2ced60fe5d3cc439bff76315e046fc2153f73af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083855"
---
# <a name="idxtkeyget_invert-method"></a>IDxtKey::get \_ Invert (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método recupera un valor booleano que indica si se invierte la operación `get_Invert` de clave. Esta propiedad se aplica a todos los tipos de clave excepto DXTKEY \_ ALPHA.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe uno de los siguientes valores.



| Value     | Descripción                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| **TRUE**  | Los píxeles de la imagen de sobrelying se invierten con respecto a la operación predeterminada. |
| **FALSE** | Los píxeles de la imagen de exceso se hacen transparentes de la manera predeterminada.         |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDxtKey (interfaz)**](idxtkey.md)
</dt> <dt>

[**IDxtKey::get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




