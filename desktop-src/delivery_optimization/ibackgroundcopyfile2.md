---
title: Interfaz IBackgroundCopyFile2 (Deliveryoptimization.h)
description: Use la interfaz IBackgroundCopyFile2 para especificar un nuevo nombre remoto para el archivo y recuperar la lista de intervalos que se van a descargar.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- Interfaz IBackgroundCopyFile2
- Interfaz IBackgroundCopyFile2, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0f185fef1ddaa9ceb4298f3e8916bb3d207b311b300f0071d601aadf47b0777a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853865"
---
# <a name="ibackgroundcopyfile2-interface"></a>Interfaz IBackgroundCopyFile2

Use la **interfaz IBackgroundCopyFile2** para especificar un nuevo nombre remoto para el archivo y recuperar la lista de intervalos que se van a descargar.

La **interfaz IBackgroundCopyFile2** hereda de la [**interfaz IBackgroundCopyFile.**](ibackgroundcopyfile.md)

Para obtener un puntero de interfaz **IBackgroundCopyFile2,** llame al método **IBackgroundCopyFile::QueryInterface** mediante __uuidof(IBackgroundCopyFile2) para el identificador de interfaz. Use el **puntero de interfaz IBackgroundCopyFile2** para llamar a los métodos [**IBackgroundCopyFile**](ibackgroundcopyfile.md) e **IBackgroundCopyFile2.**

## <a name="members"></a>Miembros

La **interfaz IBackgroundCopyFile2** hereda de [**IBackgroundCopyFile.**](ibackgroundcopyfile.md) **IBackgroundCopyFile2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IBackgroundCopyFile2** tiene estos métodos.



| Método                                                             | Descripción                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md) | Recupera la matriz de intervalos que desea descargar de la dirección URL.<br/> |
| [**SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) | Cambia el nombre remoto a una nueva dirección URL.<br/>                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 se define como 83E81B93-0873-474D-8A8C-F2018B1A939C<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> </dl>

 

 





