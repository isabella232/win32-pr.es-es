---
title: Constantes ADSI
description: En la tabla siguiente se enumeran las constantes definidas y usadas en Active Directory Interfaces de servicio (ADSI).
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
ms.openlocfilehash: 6ca2a6b7eae4550f4bbd4c8c8373d63c9bdd121e6561f08e591cb6a943d309f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023923"
---
# <a name="adsi-constants"></a>Constantes ADSI

En la tabla siguiente se enumeran las constantes definidas y usadas en Active Directory Interfaces de servicio (ADSI).



| Constante ADSI                      | Value                                   | Descripción                                                                                                                                                                                                      |
|------------------------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ EXT \_ INITCREDENTIALS**      | 1                                       | Código de control que indica que los datos personalizados proporcionados al [**método IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) contienen credenciales de usuario.                                                     |
| **ADS \_ EXT \_ INITIALIZE \_ COMPLETE** | 2                                       | Código de control que se usa con [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) para indicar que las extensiones pueden realizar cualquier inicialización necesaria, en función de las características admitidas por el objeto primario. |
| **ADS \_ EXT \_ MAXEXTDISPID**         | 16777215                                | El valor más alto de DISPID que un objeto de extensión puede usar para sus métodos y propiedades.                                                                                                                                   |
| **ADS \_ EXT \_ MINEXTDISPID**         | 1                                       | El menor DISPID que un objeto de extensión puede usar para sus métodos y propiedades.                                                                                                                                    |
| **RESPUESTA \_ DE VLV de \_ ADS**             | L"fc8cb04d-311d-406c-8cb9-1ae8b843b419" | Se usa con [**el método IDirectorySearch::GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) para recuperar los metadatos de búsqueda de VLV. Para obtener más información, [vea Cómo buscar mediante VLV.](how-to-search-using-vlv.md)        |
| **DBPROPFLAGS \_ ADSISEARCH**        | 0x0000C000                              | Se usa para trabajar con el OLE DB de trabajo.                                                                                                                                                                           |



 

 

 




