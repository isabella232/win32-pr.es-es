---
description: Las extensiones de complemento de datos adjuntos deben implementar la interfaz ISceSvcAttachmentPersistInfo.
ms.assetid: fadd2e06-d27c-4938-ad0e-ae7beab25931
title: Implementación de ISceSvcAttachmentPersistInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edaf4f31007225e95914f42d27297347799f53fe3ca2735cac38c6c0d881cebf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969332"
---
# <a name="implementing-iscesvcattachmentpersistinfo"></a>Implementación de ISceSvcAttachmentPersistInfo

Las extensiones de complemento de datos adjuntos deben implementar la [**interfaz ISceSvcAttachmentPersistInfo.**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) Los complementos configuración de seguridad consultan esta interfaz periódicamente, como al guardar la configuración o cerrar el complemento. Esto permite que la extensión de complemento guarde las modificaciones que el usuario pueda haber realizado en la base de datos de inspección o en la configuración asociada.

En el ejemplo siguiente se muestra una manera de implementar [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).


```C++
#include <windows.h>

class CSceSvcAttachmentPersistInfo:
  public ISceSvcAttachmentPersistInfo,
  public CComObjectRoot
{
    BEGIN_COM_MAP(CSceSvcAttachmentPersistInfo)
    COM_INTERFACE_ENTRY(ISceSvcAttachmentPersistInfo)
    END_COM_MAP()

    friend class CDataObject;
    friend class CComponentDataImpl;

    CSceSvcAttachmentPersistInfo();
    ~CSceSvcAttachmentPersistInfo();

public:

    // ISceSvcAttachmentPersistInfo interface members
    STDMETHOD(IsDirty)(LPTSTR lpTemplateName);
    STDMETHOD(Save)(LPTSTR lpTemplateName, SCESVC_HANDLE *pscesvcHandle,
         PVOID *ppvData, PBOOL pbOverwriteAll );
    STDMETHOD(FreeBuffer)(PVOID pvData);

    //...

};

//
// Implementing IsDirty
//
STDMETHODIMP CSceSvcAttachmentPersistInfo::IsDirty(LPTSTR lpTemplateName)
{
  if ( m_pSnapin == NULL ) 
  {
    return S_FALSE;
  }
  //
  // just calling the snap-in's main IsDirty
  //
  return m_pSnapin->IsDirty();
}

//
// Implementing Save
//
STDMETHODIMP CSceSvcAttachmentPersistInfo::Save(LPTSTR lpTemplateName,
       SCE_HANDLE *psceHandle, 
       PVOID *ppvData, 
       PBOOL pbOverwriteAll )
{
  if ( psceHandle == NULL || ppvData == NULL || 
       pbOverwriteAll == NULL ) 
  {
    return E_INVALIDARG;
  }

  if ( m_pSnapin != NULL ) 
  {

    m_pSnapin->SaveDataInBuffer(lpTemplateName, psceHandle,
       ppvData, pbOverwriteAll);

    *psceHandle = m_sceHandle;

  }

  return S_OK;
}

//
// Implementing FreeBuffer
//
STDMETHODIMP CSceSvcAttachmentPersistInfo::FreeBuffer(PVOID pvData)
{
  if ( pvData == NULL ) 
  {
    return S_OK;
  }

  PSCESVC_ANALYSIS_INFO pTempInfo=(PSCESVC_ANALYSIS_INFO)pvData;

  if ( pTempInfo->Lines != NULL ) 
  {

    for ( DWORD i=0; i < pTempInfo->Count; i++ ) 
    {

      if ( pTempInfo->Lines[i].Key != NULL )
        LocalFree(pTempInfo->Lines[i].Key);

      if ( pTempInfo->Lines[i].Value != NULL )
        LocalFree(pTempInfo->Lines[i].Value);
    }

    LocalFree( pTempInfo->Lines);
  }

  LocalFree(pTempInfo);

  return S_OK;
}
```



 

 



