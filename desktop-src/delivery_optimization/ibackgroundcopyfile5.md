---
title: Interfaz IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Use esta interfaz para obtener o establecer las propiedades genéricas de las transferencias de archivos de optimización de entrega (DO).
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
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150206"
---
# <a name="ibackgroundcopyfile5-interface"></a>Interfaz IBackgroundCopyFile5

Use esta interfaz para obtener o establecer las propiedades genéricas de las transferencias de archivos de optimización de entrega (DO).

Para obtener un puntero de interfaz **IBackgroundCopyFile5** , llame al método **IBackgroundCopyFile:: QueryInterface** mediante __uuidof (IBackgroundCopyFile5) para el identificador de interfaz.

## <a name="members"></a>Miembros

La interfaz **IBackgroundCopyFile5** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyFile5** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IBackgroundCopyFile5** tiene estos métodos.



| Método                                                  | Descripción                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyfile5-getproperty.md) | Obtiene el valor de una propiedad BackgroundCopyFile genérica.<br/> |
| [**SetProperty**](ibackgroundcopyfile5-setproperty.md) | Establece el valor de una propiedad BackgroundCopyFile genérica.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 se define como 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

