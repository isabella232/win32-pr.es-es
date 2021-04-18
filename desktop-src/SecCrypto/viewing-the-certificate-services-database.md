---
description: Los clientes autorizados correctamente utilizan la interfaz ICertView para ver la base de datos de servicios de certificados.
ms.assetid: c8f316dd-186b-4e4a-b0ce-561a23b266cb
title: Ver la base de datos de servicios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c553cee2f64c3096e733d588c9e0ad3d08ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156569"
---
# <a name="viewing-the-certificate-services-database"></a>Ver la base de datos de servicios de certificados

Los clientes autorizados correctamente utilizan la interfaz [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) para ver la base de datos de servicios de certificados. Tenga en cuentan que, como parte del producto enviado, el complemento MMC entidad de certificación se puede usar para ver la base de datos de servicios de Certificate Server. [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) se proporciona para ver la base de datos mediante programación. La compatibilidad con la interfaz **ICertView** comienza con Windows XP.

Un cliente correctamente autorizado significa a un usuario al que se le ha concedido permiso para ver la base de datos de servicios de Certificate Server; el complemento MMC entidad de certificación se puede usar para conceder o restringir el acceso para ver la base de datos (en **propiedades** de la [*entidad de certificación*](../secgloss/c-gly.md), haga clic en la pestaña **seguridad** ). Además, para usar el objeto [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) , la estación de trabajo cliente debe tener instalados los componentes de cliente de servicios de Certificate Server.

Aunque hay varios escenarios para usar [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) y sus interfaces relacionadas, a continuación se muestra una secuencia posible para desarrollar una aplicación cliente basada en **ICertView**:

**Para ver la base de datos de servicios de certificados**

1.  Después de obtener una instancia del objeto [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) , llame a [**ICertView:: OpenConnection**](/windows/desktop/api/Certview/nf-certview-icertview-openconnection) para comunicarse con una entidad de [*certificación*](../secgloss/c-gly.md) en un equipo específico.
2.  Llame a [**ICertView:: SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) para especificar el número de columnas de la vista; esta llamada también se utiliza para especificar una vista predeterminada. Si no se especifica una vista predeterminada en la llamada, el llamador debe llamar a [**ICertView:: SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn) para cada una de las columnas que se van a incluir en la vista.
3.  Opcional. Especifique los criterios de ordenación y/o los criterios de calificación para la consulta de base de datos mediante una llamada a la función [**ICertView:: SetRestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) . Los criterios de calificación consisten en informar de la vista para recuperar datos basados en calificadores como mayor que, menor que, igual a, etc.
4.  Llame a [**ICertView:: OpenView**](/windows/desktop/api/Certview/nf-certview-icertview-openview) para recuperar los datos de la vista; los datos de la vista se componen de las columnas solicitadas por medio de [**ICertView:: SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) (y si no se ha especificado una vista predeterminada, [**ICertView:: SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn)). Si se llamó a [**ICertView:: SetRestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) , los datos de las columnas se ordenarán o calificarán. **ICertView:: OpenView** crea un objeto [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) , que se puede utilizar para enumerar las filas de la vista.
5.  Use los [](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) métodos IEnumCERTVIEWROW [**IEnumCERTVIEWROW:: EnumCertViewAttribute**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewattribute), [**IEnumCERTVIEWROW:: EnumCertViewColumn**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewcolumn)y [**IEnumCERTVIEWROW:: EnumCertViewExtension**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewextension) para recuperar los datos de atributos, columnas y extensiones según sea necesario.

 

 
