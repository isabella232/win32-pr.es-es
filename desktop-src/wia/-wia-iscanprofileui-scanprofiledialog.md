---
description: Muestra un cuadro de diálogo que permite a los usuarios crear, modificar y eliminar perfiles de digitalización.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'IScanProfileUI:: ScanProfileDialog (método) (Scanprofileui. h)'
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
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276857"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a>IScanProfileUI:: ScanProfileDialog (método)

Muestra un cuadro de diálogo que permite a los usuarios crear, modificar y eliminar perfiles de digitalización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Identificador de la ventana primaria que posee el cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El cuadro de diálogo es modal; el usuario no puede cambiar a la ventana primaria hasta que se cierre el cuadro de diálogo.

Los valores del `<ProfileName>` elemento y el `<WiaItem>` elemento se pueden cambiar en el cuadro de diálogo. `<Default>`Se puede Agregar o eliminar el elemento. No se puede realizar ningún otro cambio en el perfil de digitalización en el cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Scanprofileui. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IScanProfileUI**](-wia-iscanprofileui.md)
</dt> <dt>

[Esquema de análisis de perfil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




