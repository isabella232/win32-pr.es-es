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
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888924"
---
# <a name="ibackgroundcopyfile2-interface"></a>Interfaz IBackgroundCopyFile2

Use la **interfaz IBackgroundCopyFile2** para especificar un nuevo nombre remoto para el archivo y recuperar la lista de intervalos que se van a descargar.

La **interfaz IBackgroundCopyFile2** hereda de la [**interfaz IBackgroundCopyFile.**](ibackgroundcopyfile.md)

Para obtener un puntero de interfaz **IBackgroundCopyFile2,** llame al método **IBackgroundCopyFile::QueryInterface** mediante __uuidof(IBackgroundCopyFile2) para el identificador de interfaz. Use el **puntero de interfaz IBackgroundCopyFile2** para llamar a los métodos [**IBackgroundCopyFile**](ibackgroundcopyfile.md) e **IBackgroundCopyFile2.**

## <a name="members"></a>Members

La **interfaz IBackgroundCopyFile2** hereda de [**IBackgroundCopyFile.**](ibackgroundcopyfile.md) **IBackgroundCopyFile2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IBackgroundCopyFile2** tiene estos métodos.



| Método                                                             | Descripción                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md) | Recupera la matriz de intervalos que desea descargar de la dirección URL.<br/> |
| [**SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) | Cambia el nombre remoto a una nueva dirección URL.<br/>                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                       |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| Archivo DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 se define como 83E81B93-0873-474D-8A8C-F2018B1A939C<br/>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> </dl>

 

 





