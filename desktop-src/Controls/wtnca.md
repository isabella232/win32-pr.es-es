---
title: Valores de WTNCA (Uxtheme.h)
description: Especifica marcas que modifican los atributos de estilo visual de ventana. Use uno o una combinación bit a bit de los valores siguientes.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b5528e26b7dc24a744affad84c8fd1fe74607ed1af56e20651fd43723cdbbff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059295"
---
# <a name="wtnca-values"></a>Valores de WTNCA

Especifica marcas que modifican los atributos de estilo visual de ventana. Use uno o una combinación bit a bit de los valores siguientes.



| Constante o valor                                                                                                                                                                                                                                  | Descripción                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <dt>**WTNCA \_ NODRAWCAPTION**</dt> <dt>0x00000001</dt> </dl> | Impide que se dibujara el título de la ventana.<br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <dt>**WTNCA \_ NODRAWICON**</dt> <dt>0x00000002</dt> </dl>          | Impide que se dibujara el icono del sistema.<br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <dt>**WTNCA \_ NOSYSMENU**</dt> <dt>0x00000004</dt> </dl>             | Impide que aparezca el menú de iconos del sistema.<br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <dt>**WTNCA \_ NOMIRRORHELP**</dt> <dt>0x00000008</dt> </dl>    | Impide la creación de reflejo del signo de interrogación, incluso en el diseño de derecha a izquierda (RTL).<br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <dt>**WTNCA \_ VALIDBITS**</dt> </dl>                                                                             | Máscara que contiene todos los bits válidos.<br/>                                     |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Uxtheme.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**OPCIONES \_ DE WTA**](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[**SetWindowThemeNonClientAttributes**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





