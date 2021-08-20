---
description: La notificación SPFILENOTIFY LANGMISMATCH se envía a la rutina de devolución de llamada si el idioma del archivo que se va a copiar no coincide con el idioma de un \_ archivo de destino existente.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: SPFILENOTIFY_LANGMISMATCH mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50cae8788e3ffac2de5cc7fc115b9363b8ad4591a0a4dd2447a3f86f735bec1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964473"
---
# <a name="spfilenotify_langmismatch-message"></a>Mensaje SPFILENOTIFY \_ LANGMISMATCH

La **notificación SPFILENOTIFY \_ LANGMISMATCH** se envía a la rutina de devolución de llamada si el idioma del archivo que se va a copiar no coincide con el idioma de un archivo de destino existente. Se puede enviar a la rutina de devolución de llamada por sí sola o combinada, mediante el operador OR, con [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) o [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md).


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Param1* 
</dt> <dd>

Puntero a una [**estructura FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) que contiene información sobre las rutas de acceso de los archivos de origen y de destino.

</dd> <dt>

*Param2* 
</dt> <dd>

Identifica los idiomas no coincidentes. Este miembro tiene el identificador de idioma del archivo de origen en la palabra baja y el identificador de idioma del archivo de destino existente en la palabra alta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La rutina de devolución de llamada debe devolver uno de los valores siguientes.



| Código devuelto                                                                          | Descripción                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**Verdad**</dt> </dl>  | Copie el archivo y sobrescriba el archivo existente.<br/>               |
| <dl> <dt>**Falso**</dt> </dl> | Omita la operación de copia. No sobrescriba el archivo existente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general](overview.md)
</dt> <dt>

[Notificaciones](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




