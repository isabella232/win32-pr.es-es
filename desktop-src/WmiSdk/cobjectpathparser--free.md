---
description: Método sobrecargado que libera la memoria que contiene la ruta de acceso.
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: Métodos CObjectPathParser::Free (ObjPath.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 0e7e5e366d96d4c8b5c6d82f177a480114c5d6356759c8db46389c809aea7137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819811"
---
# <a name="cobjectpathparserfree-methods"></a>CObjectPathParser::Free (Métodos)

\[La [**clase CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) forma parte del marco de proveedores WMI que ahora se considera en estado final y no habrá más desarrollos, mejoras o actualizaciones disponibles para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

Método sobrecargado que libera la memoria que contiene la ruta de acceso.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                     | Descripción                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Free(LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))                     | Libera la memoria que contiene la ruta de acceso no buscada.<br/>                      |
| [**Free(ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath)) | Libera la memoria que contiene la estructura que tiene la ruta de acceso analizada.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ObjPath.h (incluir ObjPath.h)</dt> </dl>                                                      |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

�

�
