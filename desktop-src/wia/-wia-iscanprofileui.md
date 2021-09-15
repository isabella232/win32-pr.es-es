---
description: La interfaz IScanProfileUI permite a las aplicaciones mostrar un cuadro de diálogo para que los usuarios puedan crear, modificar y eliminar perfiles de examen.
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: Interfaz IScanProfileUI (Scanprofileui.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: c8791461db76c72de81216aef188886f63fde4f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571397"
---
# <a name="iscanprofileui-interface"></a>Interfaz IScanProfileUI

La **interfaz IScanProfileUI permite** a las aplicaciones mostrar un cuadro de diálogo para que los usuarios puedan crear, modificar y eliminar perfiles de examen.

## <a name="members"></a>Members

La **interfaz IScanProfileUI** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IScanProfileUI** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IScanProfileUI** tiene estos métodos.



| Método                                                             | Descripción                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) | Muestra un cuadro de diálogo que permite a los usuarios crear, modificar y eliminar perfiles de examen.<br/> |



 

## <a name="remarks"></a>Observaciones

El cuadro de diálogo es modal; El usuario no puede cambiar a la ventana primaria hasta que se cierre el cuadro de diálogo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                        |
| Encabezado<br/>                   | <dl> <dt>Scanprofileui.h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Esquema de perfil de examen](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
