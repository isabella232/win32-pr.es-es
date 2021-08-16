---
description: Muestra un cuadro de diálogo que permite a los usuarios crear, modificar y eliminar perfiles de examen.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: Método IScanProfileUI::ScanProfileDialog (Scanprofileui.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: a2003471a151677b5f0fbd9ae88e9d3cf8d975525a9dbf8340c6fc1a9f2befc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965814"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a>IScanProfileUI::ScanProfileDialog (método)

Muestra un cuadro de diálogo que permite a los usuarios crear, modificar y eliminar perfiles de examen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Tipo: **HWND**

Identificador de la ventana primaria propietaria del cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El cuadro de diálogo es modal; El usuario no puede cambiar a la ventana primaria hasta que se cierre el cuadro de diálogo.

Los valores del `<ProfileName>` elemento y del elemento se pueden cambiar en el cuadro de `<WiaItem>` diálogo. El `<Default>` elemento se puede agregar o eliminar. No se puede realizar ningún otro cambio en el perfil de examen en el cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Scanprofileui.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IScanProfileUI**](-wia-iscanprofileui.md)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




