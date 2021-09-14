---
description: Los clientes autorizados correctamente usan la interfaz ICertView para ver la base de datos de Servicios de certificados.
ms.assetid: c8f316dd-186b-4e4a-b0ce-561a23b266cb
title: Ver la base de datos de Servicios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c553cee2f64c3096e733d588c9e0ad3d08ceb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170830"
---
# <a name="viewing-the-certificate-services-database"></a>Ver la base de datos de Servicios de certificados

Los [**clientes autorizados correctamente**](/windows/desktop/api/Certview/nn-certview-icertview) usan la interfaz ICertView para ver la base de datos de Servicios de certificados. Debe tenerse en cuenta que, como parte del producto enviado, el complemento MMC de la entidad de certificación se puede usar para ver la base de datos de Servicios de certificados. [**ICertView se**](/windows/desktop/api/Certview/nn-certview-icertview) proporciona para ver la base de datos mediante programación. La compatibilidad con **la interfaz ICertView** comienza con Windows XP.

Un cliente autorizado correctamente significa un usuario al que se le ha concedido permiso para ver la base de datos de Servicios de certificados; El complemento MMC de entidad de certificación se puede usar para  conceder o restringir el acceso para ver la base de datos (en Propiedades de la entidad de [*certificación*](../secgloss/c-gly.md), haga clic en **la pestaña** Seguridad). Además, para usar el [**objeto ICertView,**](/windows/desktop/api/Certview/nn-certview-icertview) es necesario que la estación de trabajo cliente tenga instalados los componentes de cliente de Servicios de certificados.

Aunque hay varios escenarios para usar [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) y sus interfaces relacionadas, a continuación se muestra una posible secuencia para desarrollar una aplicación cliente basada en **ICertView**:

**Para ver la base de datos de Servicios de certificados**

1.  Después de obtener una instancia del objeto [**ICertView,**](/windows/desktop/api/Certview/nn-certview-icertview) llame a [**ICertView::OpenConnection**](/windows/desktop/api/Certview/nf-certview-icertview-openconnection) para comunicarse con una entidad de [*certificación*](../secgloss/c-gly.md) en un equipo específico.
2.  Llame [**a ICertView::SetResultColumnCount para**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) especificar el número de columnas de la vista; Esta llamada también se usa para especificar una vista predeterminada. Si no se especifica una vista predeterminada en la llamada, el autor de la llamada debe llamar a [**ICertView::SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn) para cada una de las columnas que se incluirán en la vista.
3.  Opcional. Especifique criterios de ordenación o criterios de calificación para la consulta de base de datos mediante una llamada a la [**función ICertView::SetRestriction.**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) Los criterios de calificación consisten en informar a la vista para que recupere datos basados en calificadores como Mayor que, Menor que, Igual a, y así sucesivamente.
4.  Llame [**a ICertView::OpenView para**](/windows/desktop/api/Certview/nf-certview-icertview-openview) recuperar los datos de la vista; Los datos de la vista contendrán las columnas solicitadas por medio de [**ICertView::SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) (y si no se especificó una vista predeterminada, [**ICertView::SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn)). Si se llamó a [**ICertView::SetRestriction,**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) los datos de las columnas se ordenarán o calificarán. **ICertView::OpenView** crea un objeto [**IEnumCERTVIEWROW,**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) que se puede usar para enumerar las filas de la vista.
5.  Use los métodos [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) [**IEnumCERTVIEWROW::EnumCertViewAttribute**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewattribute), [**IEnumCERTVIEWROW::EnumCertViewColumn**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewcolumn)e [**IEnumCERTVIEWROW::EnumCertViewExtension**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewextension) para recuperar los datos de atributo, columna y extensión según sea necesario.

 

 
