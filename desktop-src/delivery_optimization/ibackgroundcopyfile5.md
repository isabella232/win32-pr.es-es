---
title: Interfaz IBackgroundCopyFile5 (Deliveryoptimization.h)
description: Use esta interfaz para obtener o establecer propiedades genéricas de Optimización de distribución de archivos.
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- Interfaz IBackgroundCopyFile5
- Interfaz IBackgroundCopyFile5, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8274d256399efbf03f1365e55609bc601590ee47
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128519947"
---
# <a name="ibackgroundcopyfile5-interface"></a>Interfaz IBackgroundCopyFile5

Use esta interfaz para obtener o establecer propiedades genéricas de Optimización de distribución de archivos.

Para obtener un puntero de interfaz **IBackgroundCopyFile5,** llame al método **IBackgroundCopyFile::QueryInterface** mediante __uuidof(IBackgroundCopyFile5) para el identificador de interfaz.

## <a name="members"></a>Miembros

La **interfaz IBackgroundCopyFile5** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyFile5** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IBackgroundCopyFile5** tiene estos métodos.



| Método                                                  | Descripción                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**Getproperty**](ibackgroundcopyfile5-getproperty.md) | Obtiene el valor de una propiedad BackgroundCopyFile genérica.<br/> |
| [**Setproperty**](ibackgroundcopyfile5-setproperty.md) | Establece el valor de una propiedad BackgroundCopyFile genérica.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 se define como 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

