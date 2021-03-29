---
title: Constantes ADSI
description: En la tabla siguiente se enumeran las constantes definidas y utilizadas en Active Directory interfaces de servicio (ADSI).
ms.assetid: facc00e8-2ecd-4428-bddd-cfa1ff1b8538
ms.tgt_platform: multiple
keywords:
- ADS_EXT_INITCREDENTIALS
- ADS_EXT_INITIALIZE_COMPLETE
- ADS_EXT_MAXEXTDISPID
- ADS_EXT_MINEXTDISPID
- ADS_VLV_RESPONSE
- DBPROPFLAGS_ADSISEARCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc4aaf5043f9fcd2a61dfa68124b6cb1a1a69b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773021"
---
# <a name="adsi-constants"></a>Constantes ADSI

En la tabla siguiente se enumeran las constantes definidas y utilizadas en Active Directory interfaces de servicio (ADSI).



| ADSI (constante)                      | Value                                   | Descripción                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **INITCREDENTIALS de ADS \_ ext \_**      | 1                                       | Código de control que indica que los datos personalizados proporcionados al método [**IADsExtension:: Operating**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contienen las credenciales de usuario.                                                     |
| **\_ \_ finalización de la inicialización de ADS \_** | 2                                       | Código de control que se usa con [**IADsExtension:: Operating**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) para indicar que las extensiones pueden realizar cualquier inicialización necesaria, en función de las características admitidas por el objeto primario. |
| **MAXEXTDISPID de ADS \_ ext \_**         | 16777215                                | El DISPID más alto que un objeto de extensión puede usar para sus métodos y propiedades.                                                                                                                                   |
| **MINEXTDISPID de ADS \_ ext \_**         | 1                                       | El DISPID más bajo que un objeto de extensión puede usar para sus métodos y propiedades.                                                                                                                                    |
| **\_respuesta VLV de ADS \_**             | L "fc8cb04d-311D-406c-8cb9-1ae8b843b419" | Se usa con el método [**IDirectorySearch:: getcolumn (**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para recuperar los metadatos de búsqueda VLV. Para obtener más información, consulte [Cómo buscar con VLV](how-to-search-using-vlv.md).        |
| **DBPROPFLAGS \_ ADSISEARCH**        | 0x0000C000                              | Se utiliza para trabajar con el proveedor de OLE DB.                                                                                                                                                                           |



 

 

 




