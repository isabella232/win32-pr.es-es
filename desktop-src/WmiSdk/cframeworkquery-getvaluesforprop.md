---
description: El método GetValuesForProp devuelve todos los valores de una propiedad determinada generados por esa propiedad tal y como aparece en la consulta.
audience: developer
ms.assetid: b5ed4b48-f622-4a55-897d-d800ada0270f
ms.tgt_platform: multiple
title: 'Métodos CFrameworkQuery:: GetValuesForProp (FrQuery. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b5fd9dbc22289843141c517203809045abbf05a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277941"
---
# <a name="cframeworkquerygetvaluesforprop-methods"></a>CFrameworkQuery:: GetValuesForProp (métodos)

\[La clase [**CFrameworkQuery**](/windows/win32/api/frquery/nl-frquery-cframeworkquery) forma parte del marco de trabajo del proveedor WMI, que ahora se considera en el estado final, y no habrá más desarrollo, mejoras o actualizaciones para problemas no relacionados con la seguridad que afecten a estas bibliotecas. Las [API de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) deben usarse para todo el desarrollo nuevo.\]

El método **GetValuesForProp** devuelve todos los valores de una propiedad determinada generados por esa propiedad tal y como aparece en la consulta.

Por ejemplo, una llamada a **GetValuesForProp**(L "Name", SA) devuelve la matriz *SA*, que contiene todos los valores de "Name" que requieren que se devuelvan instancias para satisfacer la consulta. Si *SA* contiene {"a", "b"}, todas las instancias donde "Name = a" más todas las instancias donde "Name = b" se deben devolver para satisfacer completamente la consulta.

Si las restricciones en "Name" no están suficientemente limitadas, se devuelve una matriz *SA* vacía.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                                             | Descripción                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetValuesForProp (CHStringArray&, LPCWSTR)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_chstringarray_))                      | Devuelve todos los valores de una propiedad determinada generados por esa propiedad tal y como aparece en la consulta.<br/> |
| [**GetValuesForProp (LPCWSTR, STD:: Vector &lt; \_ bstr \_ t &gt;&)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_std-vector__bstr_t__)) | Devuelve todos los valores de una propiedad determinada generados por esa propiedad tal y como aparece en la consulta.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>FrQuery. h (incluye FwCommon. h)</dt> </dl>                                                     |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| Archivo DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
